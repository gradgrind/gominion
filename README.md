# gominion
MINION parser/writer for Go

MINION is a mark-up language for simple data transfer, configuration files, etc. – similar to JSON, but with more emphasis on writing manually.

JSON is actually valid MINION, but not necessarily the other way round. MINION is simpler in the sense that it has no data types apart from strings, but extends JSON in a few ways to make it more convenient for writing by hand. See [minion.md](doc/minion.md) for more details.

`gominion` is a Go deserializer/serializer (parser/writer) for MINION. At present the serializer quotes all strings, producing valid JSON.

A simple test file is included, `minion_test.go`.

I have tried to provide helpful error messages, but no i18n is supported at present.

Maps are represented as arrays of key/value pairs. This has the (possible) advantage of retaining input order trivially, but can be inefficient when the number of keys grows.

The code has been subject to only limited testing.
