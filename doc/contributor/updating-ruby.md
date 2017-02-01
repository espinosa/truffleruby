# Updating our version of Ruby

First, check with Chris Seaton for clearance.

From MRI copy and paste over our versions of:

* `lib` to `lib/mri`
* `ext/{bigdecimal,psych,pty}/lib` to `lib/ext`
* `test/mri`
* `doc/legal/ruby-bsdl.txt` and `doc/legal/ruby-licence.txt`

The script `tool/update-mri.sh` will do the above for you, assuming you have the
version of MRI you want checked out in `../ruby`. You should be able to commit
changes from this script without modification. If you can't, you need to update
the script or these instructions.

* `-h` and `--help` output in `CommandLineParser`
* `lib/json` using the version of `flori/json` specified but not totally included in `ext/json`

Check for changes that we need to match in some way in other code, or legal
questions.

* Update version information in `RubyLanguage`
* Update `doc/user/compatibility.md`
