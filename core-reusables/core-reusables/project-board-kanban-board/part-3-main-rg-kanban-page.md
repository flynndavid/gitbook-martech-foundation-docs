# Part 3: Main RG Kanban Page

{% embed url="https://www.loom.com/embed/390c40917bdc47689f00f4b43d5153d1?sid=4aee310d-2742-4667-be59-5e2fbe062dc2" %}

## Setting up the Kanban Board in the Editor <a href="#documentation-setting-up-the-kanban-board-in-the-editor" id="documentation-setting-up-the-kanban-board-in-the-editor"></a>

To set up the Kanban board in the editor, follow these steps:

1. Use the `Draggable Elements` plugin by Bubble instead of the `Drag and Drop Reorder RG`.
2. Create an `RG Kanban Column` for the horizontal setup, displaying stages like lead, pending, and in-progress.
3. Place an `RG Kanban Status Columns` element with one row above the `RG Kanban Item` for the vertical elements.
4. Add a `Drop Area Kanban Stages` group above the `RG Kanban Item` and place the `RG Kanban` inside it.
5. In the workflows, ensure that the `Drop Area Kanban Stages` has a group `DragDrop` on it and `Current User's Date Signup Complete` is not empty.
6. In the workflow, when the drop area changes, update the project's stage based on the stage it was dragged to.
7. Use the edit icons to edit stages on the vertical cards.
8. Utilize the reusable element for editing specific projects on the vertical cards.

That's all you need to do to set up the Kanban board in the editor. If you need further assistance, feel free to reach out on Discord. Thank you for watching!
