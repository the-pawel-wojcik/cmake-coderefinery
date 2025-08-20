# 6. Creating and running tests with CTest

See the list of all cmake properties
```bash
cmake --help-properties
# the same as
man 7 cmake-properties
```
Search for "Properties on Tests"

Selection of `ctest`'s flags
```bash
ctest -N  # don't run, only list tests
ctest -V  # verbose
ctest -VV  # extra verbose
ctest -R REGEX  # run tests with names matching the REGEX
ctest -RE REGEX  # exclude tests with names matching the REGEX
ctest -L REGEX  # run tests with labels matching the REGEX
ctest -LE REGEX  # exclude tests with labels matching the REGEX
ctest --rerun-failed
```
