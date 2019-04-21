To solve running non-repeatable job in an autoscale cluster problem.


Usage:

```
lock:= dlock.NewDLock(db)

success := lock.Lock("task-1", 10*time.Minute)
if !success{
    return
}
defer lock.UnLock("task-1")

...do task-1 code...

```
