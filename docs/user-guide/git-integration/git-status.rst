Git Status
==========

Sparkflows can show the changes yet to be pushed to Git via the ``Git Status`` Button. 

To access ``Git status``, open a project and select ``Workflows``. You would see a page similar to below.

.. figure:: ../../_assets/git/git_wf_status.PNG
   :alt: git-status
   :width: 70%

When ``Git Status`` is clicked you would be redirected to another page where you can see the list of workflows that have not been pushed to Git. You would see a page similar to below.

.. figure:: ../../_assets/git/git-status-list.png
   :alt: git-status
   :width: 70%

Upon clicking the workflow name you would see Workflow JSON differences between the current JSON and last workflow JSON pushed to Git as seen in the image below. If the workflow has not been pushed to Git before, a pop up would show up stating ``There is no previous version available to show the diff``.

.. figure:: ../../_assets/git/git-status-json-differences.png
   :alt: git-status
   :width: 70%

- To see the differences in workflow form click the ``Workflow`` tab. 

.. figure:: ../../_assets/git/git-status-wf-differences.PNG
   :alt: git-status
   :width: 70%

- If there are no differences to show the  message ``No diff to show!`` is shown.

.. figure:: ../../_assets/git/git-status-no-differences.png
   :alt: git-status
   :width: 70%
