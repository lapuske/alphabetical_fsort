alphabetical_fsort
==================

Command-line utility sorting files in alphabetical order.

For example, it can be used to sort Fluent localization keys and labels. The utility preserves the license header, if any.



## Usage

First of all, add the package to your `pubspec.yaml`:

```yaml
dev_dependencies:
  alphabetical_fsort:
    url: https://github.com/lapuske/alphabetical_fsort.git
```

Then you can execute `dart run alphabetical_fsort` in order to sort the files.

```bash
dart run alphabetical_fsort.dart
```

#### Exit instead of applying the sorting

```bash
dart run alphabetical_fsort.dart --exit
```

#### Custom locations

```bash
# Specify a custom file to sort.
dart run alphabetical_fsort.dart \
         --target=assets/l10n/en-ES.ftl

# Specify a whole directory to sort the files within (not recursive).
dart run alphabetical_fsort.dart \
         --target=assets/l10n/
```



## Exit flags

- 0, on success.
- 1, when sorting is required (applicable when `--exit` flag is provided).
- 64, when invalid arguments are passed.
- 66, when input files can't be found.