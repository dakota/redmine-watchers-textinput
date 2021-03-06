redmine-watchers-textinput
==========================

This is a plugin that replaces the checkboxes for adding watchers with a nice, tokenized text input with autocomplete. The actual Redmine plugin name is "watchers_textinput". The pages that are modified are the "Add new issue" page and "Edit watchers" (on existing issue) popup.

I installed Redmine at my company, but we have around 100 engineers, and people were complaining the checkboxes are annoying to use (and take up a lot of space). 

This plugin effectively still uses the checkbox inputs but makes them hidden. The autocomplete script effectively reads what's in the checkboxes to get the list of users, and will "check" in the checkboxes. This way I didn't have to change what the server-side is expecting in the form submission.

It does at least replace one view (*erb) so it is probably not super portable.

The actual autocomplete plugin used is Select2 (http://ivaynberg.github.io/select2/)

To install run in redmine root:
```
git clone https://github.com/alvinchow86/redmine-watchers-textinput.git plugin/watchers_textinput
```
