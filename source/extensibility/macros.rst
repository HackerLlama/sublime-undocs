======
Macros
======

Macros are a basic automation facility comprising sequences of commands. Use
them whenever you need to repeat the exact same steps to perform an operation.

Macro files are JSON files with the extension ``.sublime-macro``. Sublime Text
ships with a few macros providing core functionality, such as line and word
deletion. You can find these under **Tools | Macros**.

How to Record Macros
********************

To start recording a macro, press :kbd:`Ctrl+q` and subsequently execute the
desired steps one by one. When you're done, press :kbd:`Ctrl+q` again to stop
the macro recorder. Your new macro won't be saved to a file, but kept in the
macro buffer instead. Now you will be able to run the recorded macro by
pressing :kbd:`Ctrl+Shift+q`, or save it to a file by selecting
**Tools | Save macro...**

Note that the macro buffer will remember only the latest recorded macro. Also,
macros only record commands sent to the buffer: window-level
commands, such creating a new file, will be ignored.

How to Edit Macros
******************

As an alternative to recording a macro, you can edit it by hand. Just save a new file
with the extension ``.sublime-macro`` under :file:`Packages/User` and add
commands to it. Macro files have this format::

   [
       {"command": "move_to", "args": {"to": "hardeol"}},
       {"command": "insert", "args": {"characters": "\n"}}
   ]

See the :doc:`../core/commands` section for more information on commands.

.. XXX: do we need to escape every kind of quotations marks?

If you're editing a macro by hand, you need to escape quotation marks,
blank spaces and backslashes by preceding them with ``\``.

Where to Store Macros
*********************

Macro files can be stored in any package folder, and then will show up
under **Tools | Macros | <PackageName>**.


