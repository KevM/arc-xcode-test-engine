## 3.0.3

* Resolved coverage failure with Xcode 7.3 and newer. Thanks to [aelam](https://github.com/aelam) for filing [#2](https://github.com/google/arc-xcode-test-engine/issues/2).

## 3.0.2

* Resolves crash caused by referencing the wrong stderr variable. The error was
  `Attempt to read from undeclared property XcodeUnitTestEngine::stderr`.

## 3.0.1

* If tests fail to build we no longer generate a
  `Unhandled Exception ("PhutilTypeMissingParametersException")` exception on Phabricator. We were
  not previously providing a name to the ArcanistUnitTestResult instance.

## 3.0.0

* Commands now always run from the root directory of the project rather than from the shell's
  current working directory. This may be a breaking change.

## 2.1.1

* Improved overall test parsing time by approximately 50%.

## 2.1.0

* Added a `pre-build` configuration option.

## 2.0.2

* Error line detection is now more flexible. Any output line with "error:" will be detected and
  bubble up as an error.

## 2.0.1

* Better handling of non-unit-test failures, such as CocoaPods getting out of sync.

## 2.0.0

* Coverage is now enabled and **reported** unless explicitly disabled with --no-coverage.
* xcodebuild or llvm-cov failures now properly throw exceptions rather than silently continuing.

## 1.1.0

* Coverage is now enabled unless explicitly disabled with --no-coverage.

## 1.0.1

* Don't run unit tests if no files were provided to the engine and we're not being asked
  to run all tests.

## 1.0.0

* Initial release.
* Provides `arc unit` and `arc unit --coverage` support for a single xcode project/target
  per-project.
