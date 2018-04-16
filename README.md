pouchdb-replication
======

****** kdoran edit *******
This is a custom build of the `pouchdb-replication` package. How this build was made:
1. cloned pouchdb/pouchdb at 6.4.3 (latest release)
2. build it
3. made `node_modules/packages/pouchdb-replication` into a git repository
4. manually applied this fix: https://github.com/pouchdb/pouchdb/commit/52a6e92f5c825cadfa6c3878c5ad24f944c0dca2
5. included this project as a node module  

This is intended to be temporary until the next PouchDB release includes that batch replication id fix (52a6e92f5c825cadfa6c3878c5ad24f944c0dca2).

****** end edit *******

PouchDB's replication and sync algorithm, as a plugin.

### Usage

```bash
npm install pouchdb-replication
```

```js
PouchDB.plugin(require('pouchdb-replication'));
var db = new PouchDB('mydb');
db.replicate(/* see replicate/sync API docs for full info */);
```

For full API documentation and guides on PouchDB, see [PouchDB.com](http://pouchdb.com/). For details on PouchDB sub-packages, see the [Custom Builds documentation](http://pouchdb.com/custom.html).

### Source

PouchDB and its sub-packages are distributed as a [monorepo](https://github.com/babel/babel/blob/master/doc/design/monorepo.md).

For a full list of packages, see [the GitHub source](https://github.com/pouchdb/pouchdb/tree/master/packages).
