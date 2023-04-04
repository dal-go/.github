# Dalgo - Data Access Layer in GO language

Provides a consistent and flexible API for working with different types of databases in Go. By providing a single interface for different types of databases, Dalgo allows developers to write code that is agnostic to the underlying data store. This can help reduce development time and improve code maintainability, while also providing the flexibility to choose the data store that best suits their needs.

It includes an easy-to-use API for querying, inserting, updating, and deleting records, as well as features for handling errors and logging. It also supports transactions.

## 📦 Modules & Packages

- [github.com/dal-go/dalgo](https://github.com/dal-go/dalgo) - core package. Go there for docs & more details. Consider giving it a ⭐ 😉.

## 🧪 Mocks for your tests
- [github.com/dal-go/mocks4dalgo](https://github.com/dal-go/mocks4dalgo) - makes testing your code that uses Dalgo easier.

## 🔌 Adapters to databases
- [github.com/dal-go/dalgo2sql](https://github.com/dal-go/dalgo2sql) - uses standard Go `database/sql` package.
- [github.com/dal-go/dalgo2firestore](https://github.com/dal-go/dalgo2firestore) - bridge to Google Firestore.
- [github.com/dal-go/dalgo2datastore](https://github.com/dal-go/dalgo2datastore) - Google Cloud Datastore (App Engine).
- [github.com/dal-go/dalgo2badger](https://github.com/dal-go/dalgo2badger) - Badger is a DB written in Go that can persist to local storage.
- [github.com/dal-go/dalgo2buntdb](https://github.com/dal-go/dalgo2buntdb) - BuntDB is in-memory DB written in Go.

# 🍿 Demo & Examples of usage
- [github.com/dal-go/dalgo-demo](https://github.com/dal-go/dalgo-demo)
