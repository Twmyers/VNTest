



# Delete a Plan

When you delete a plan, other plans might be affected. Use caution when
selecting plans to delete and when selecting the following deletion
options:

- **Cascade**: The selected plan and all child plans are deleted
- **Selected plan only**: Only the selected plan is deleted. If there
  are child plans, their source plan is removed or replaced.



To delete a plan, you must be the only user logged into the project and
the project must be locked to prevent orphaned data. See Lock or Unlock
a Project. If you are the only user logged into the project and you do
not lock the project prior to deleting a plan, the project is locked
automatically and unlocked when the deletion is complete.



To delete a plan

1.  In the **Tools** menu, point to **Global Project Data** and select
    **Plans**.
2.  In the **Plans** dialog box, click the plan you want to delete and
    click **Remove**.
3.  Select one of the following options:
    | Option | Description |
| --- | --- |
| Cascade | Deletes the selected plan and all descendant plans. This option is only enabled when deleting a plan with descendants. |
| Selected plan only | Only deletes the selected plan. Does not delete the selected plan’s descendants. Deleting a top level plan: All direct descendants (children) become top level plans. The source plan for all indirect descendants does not change. Deleting a child plan: If you delete a child plan with direct descendants (children), the source plan of those descendants is changed to the source plan of the plan you are deleting. The source plan for all indirect descendants does not change. |

4.  Click **OK**.\
    If you have not locked the project (but you are the only user logged
    in), a warning informs you that the project will be locked
    automatically.
5.  Click **Yes** to continue.
