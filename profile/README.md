# [DALgo](https://dalgo.io/) - Database Abstraction Layer in Go language

https://dalgo.io/

Provides a consistent, flexible & implementation agnostic Go API for working with different types of databases.
By providing a single interface for different types of databases, Dalgo allows developers to write code that is agnostic to the underlying data store.
This can help reduce development time and improve code maintainability, while also providing the flexibility to choose the data store that best suits their needs.

It includes an easy-to-use API for querying, inserting, updating, and deleting records, as well as features for handling errors and logging. It also supports transactions.

## 🛡️ Portable Access Policies

DALgo can turn any database handle into an adapter-independent capability:
extensions, tenants, background jobs, analytics, and support tools receive only
the paths and operations they need. The boundary covers point reads, queries,
batches, mutations, and transactions before an adapter is called.

- Hierarchical `Allow(path).Deny(subpath)` and
  `Deny(path).Allow(selectedSubpaths...)` rules.
- Independent `Get`, `Exists`, `Query`, `Insert`, `Set`, `Update`, `Delete`,
  and reserved `Truncate` permissions—write never implies read.
- Global and context-bound policies compose by intersection, so added policy
  layers can only narrow access.
- YAML-first, JSON-equivalent documents load from any storage through
  `io.Reader`.
- Custom SQL text is an opaque query capability, denied unless a policy grants
  it explicitly; path rules never authorize SQL by parsing its text.
- Explainable denials identify the operation, resource, policy source, and
  winning rule for trusted logs and developer tooling.
- The same matcher supports independent audit-event selection without
  granting data access.

Explore the [interactive access-policies overview](https://dalgo.io/access-policies/)
or read the [complete repository guide](https://github.com/dal-go/dalgo/blob/main/docs/access-policies.md).

## 📦 Modules & Packages

- [`github.com/dal-go/dalgo`](https://github.com/dal-go/dalgo) - core package. Go there for docs & more details. Consider giving it a ⭐ 😉.

### 🧪 Mocks for your tests
- [`github.com/dal-go/mocks4dalgo`](https://github.com/dal-go/mocks4dalgo) - makes testing your code that uses Dalgo easier.

### 🔌 Adapters to databases
- [`github.com/dal-go/dalgo2sql`](https://github.com/dal-go/dalgo2sql) - uses standard Go `database/sql` package.
- [`github.com/dal-go/dalgo2firestore`](https://github.com/dal-go/dalgo2firestore) - bridge to Google Firestore.
- [`github.com/dal-go/dalgo2datastore`](https://github.com/dal-go/dalgo2datastore) - Google Cloud Datastore (App Engine).
- [`github.com/dal-go/dalgo2badger`](https://github.com/dal-go/dalgo2badger) - Badger is a DB written in Go that can persist to local storage.
- [`github.com/dal-go/dalgo2buntdb`](https://github.com/dal-go/dalgo2buntdb) - BuntDB is in-memory DB written in Go.

All qualified adapters are passing [`dalgo-end2end-tests`](https://github.com/dal-go/dalgo-end2end-tests). If you developed an adapter and it passes the end-to-end tests it can be added here - please submit a PR.

# 🍿 Demo & Examples of usage
- [github.com/dal-go/dalgo-demo](https://github.com/dal-go/dalgo-demo)

# 🔥 Used by
- [`github.com/bots-go-framework`](https://github.com/bots-go-framework)
- [datatug-cli](https://github.com/datatug/datatug-cli) - Context-aware data viewer & collaborative query manager for effortless exploration of related data — CLI + Web UI

Submit a PR for adding a link here if you use Dalgo in your open source project.
