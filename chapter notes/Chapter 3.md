

log 
- single, atomic operation on a state machine
- append-only sequence of records



Logs used in:
1. storage engines, db replication, system durability and integrity (WAL)
2. consensus (raft)
3. PostgreSQL - WAL (write-ahead log)
4. front end state tracking (redux)
5. version control commit logs

Log made of :
- segments, active segment
- segment has index file, store file


1. mmap file truncation - because we cannot resize once memory-maped
2. code doesn't handle ungraceful shutdowns - have to do sanity checks ideally
3. RWMutex. Could be further optimized by putting mutex per segment
4. 




References -
1. [mmap](https://youtu.be/nPIhoJ6lKeQ)
   1. [endianness](https://www.youtube.com/watch?v=NcaiHcBvDR4)
   
TODOS -
1. Dig more on mmap and file organization in memory
   1. 
2. buffered writer (vs) direct file writing
   1. [streams and buffers](https://medium.com/rungo/introduction-to-streams-and-buffers-d148c0cda0ad)
   2. [bufio](https://www.educative.io/edpresso/how-to-read-and-write-with-golang-bufio)
3. io.MultiReader


Doubts/Ponder:
1. Mutex on segments - how/why is it better ?
2. 



