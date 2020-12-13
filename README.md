# simple implementation of raft consensus algorithm

---

### TODO
- [x] Leader election
- [x] Log replication

### Branch
- master： Leader election & Log replication
- election：Leader election
- replication：Log replication

### build
```
go build -o simple-raft
```

### run
```
go get go get github.com/mattn/goreman
goreman start
./simple-raft --id 1 --cluster 127.0.0.1:22379,127.0.0.1:32379 --port :12379
./simple-raft --id 2 --cluster 127.0.0.1:12379,127.0.0.1:32379 --port :22379
./simple-raft --id 3 --cluster 127.0.0.1:12379,127.0.0.1:22379 --port :32379
```

