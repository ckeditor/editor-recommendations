---
usability:
  title: "Inline style state"
  description: Draft for Inline style state behavior in WYSIWYG.
  status: "Draft"
  discussion: "https://github.com/ckeditor/editor-recommendations/issues/32"

layout: default
---

{% capture description %}

Inline styles (like bold, italic or strikethrough) might be active or inactive. This information is both for user experience and have an impact on editor behavior. It is very important to correctly set style state because it has big impact on UX. There are multiple situations when deducing style state is not trivial and the editor is expected to make educated guess to enable better experience for the user.

{% endcapture %}

{% capture expectations %}
Inline style state is represented through UI, most often by changing the look of the button connected with certain feature. Style state has different meaning, depending whether some content in the editor is selected or not.

If content is selected, it is expected that style state reflects state of that content. For example, if bold text is selected, bold style state should be "active" to:

* inform the user,
* un-bold the selected text if the user uses bold feature

If content is not selected, it is expected that newly typed text will have applied all active styles. For example, if user placed caret somewhere in the content and used bold feature, it state should become "active" and any typed character should have bold applied. After using bold feature again, it's state should become "inactive".

{% endcapture %}

{% capture recommendations %}

## Problems to Solve

1. Selection has content with different styles applied.
2. Selection has content which cannot have certain style applied (for example image cannot have italic style applied).
3. Selection is done backwards (anchor position is after focus position).
4. Selection has multiple ranges in it.
5. Caret is placed between two characters with different styles.
6. Caret is placed in new or empty paragraph.
7. What should happen when user removes selected content.

## Proposals

### 1. Selection Has Content With Different Styles Applied.

If style state cannot be directly reflected by selection content, it should reflect what is expected editor behavior.

*If it is expected that selected content should be wholly bold after using bold feature, the style state should be "inactive". It may be wise to set style to inactive if there is at least one inactive element in selection, because if the user wanted to remove a style, they would be more precise in selecting exactly the part to remove. However this behavior probably needs more argumentation*

*On the other hand, if user types a new letter with selection set it may be expected that the newly typed character have same styles as the place where it will be put and certainly it should have styles reflecting as styles states. If selection is on **f[o**b**a]r** and bold state is inactive, what should be style of newly typed letter?*

*What if given style have multiple possible values? I.e. font color.*

### 2. Selection Has Content Which Cannot Have Certain Style Applied.

As long as there is content that is applicable for given style, content that cannot be styled should not have any impact on style state.

### 3. Selection Is Done Backwards.

*Note: just basing on browsers, this should not have any impact on style state. This makes sense, because style state should be connected with selection contents and not the way it was made.*

### 4. Selection Has Multiple Ranges in It.

Each range should be checked in same way as single-range selection and the results should be "added". For example, if one range has only bold text but the other range has non-bold text, style state should be "inactive".

*Argumentation needed?*

### 5. Caret Is Placed Between Two Characters With Different Styles.

Similar to 1. Style state should reflect state of character before or after caret. Sometimes there might be no characters before/after, i.e. when caret is at the beginning or end of paragraph, or before or after an image). By default it is advised to first look left because it is expected that the user want to continue typing in the context before the caret.

*There is a nice feature in Firefox, though. When user uses left and right arrows to navigate caret through content, the caret looks at the side it "came from". So, when user clicks left, the caret looks to right. For example, if caret was in bold text and by arrows it was moved to a place between bold and non-bold character, style state remain bolded. This could called "style retention". It greatly enhances UX by giving the user more ability to manipulate style state.*

### 6. Caret Is Placed in New or Empty Paragraph.

When user creates new paragraph it is expected that they want to use same styles that before breaking the paragraph. Style state should be retained. When navigating to empty paragraph, styles states should be recovered to the last known styles states encountered in that paragraph.

*Argumentation needed?*

### 7. What Should Happen When User Removes Selected Content.

After user removes selected content it is expected that they want to continue typing in the context before the caret. Styles state should be taken from the character before.

*Argumentation needed?*

## Styles Decision Algorithm Proposal

Taken into consideration question and answers above, this is a proposal of algorithm for deciding styles state when selection is made in editor or caret position is changed.

1. If selection is not-collapsed look at the first character in the selected range and set styles state basing on it.
2. If selection is collapsed or there were no characters in range, look at the node before caret position. If it's a character, set styles state basing on it.
3. If not, look at the node after caret position. If it's a character, set styles state basing on it.
4. If not, try to find a first character that is on left of caret (to the beginning of text container) and if found, set styles basing on it.
5. If not found, try to find a first character that is on the right of caret (to the end of text container) and if found, set styles basing on it.
6. If not found it means that there are no characters in caret container. Load last remembered styles states for this container.

{% endcapture %}

{% capture references %}

1. [An issue in CKEditor 4 tracker: *Impossible to place caret in an empty inline style that existed in an empty block*](https://dev.ckeditor.com/ticket/12634).

{% endcapture %}

{% include usability.html %}
