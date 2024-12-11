# Lingui Origin Comments Overwritten MCVE

This is a minimal, complete, verifiable example of a bug in Lingui where existing origin comments are overwritten when extracting an existing message from a new file.

## Steps to reproduce

1. Add a message that already exists to a new file. In this reproduction, this has already been done – see commit `616e5c1`.
2. Run `lingui extract <path-to-new-file>`.

## Expected behaviour

The path to the location of the message in the new file is appended to the list of paths for the message in the translation file.

## Actual behaviour

The path to the location of the message in the new file replaces the existing path.
