# Decal 3.0 (2.9.7.5) / Decal.Adapter.dll Change Log

### 2017-11-24
[Mag-nus]
* Previous changes didn't pan out so I started from a fresh, unmodified dll.
* Strong-Named signature removed from assembly
* Decal.Adapter.IDQueue.FairRoundRobinScheduleQueue.DeleteAction changed from void to bool return type.
* Decal.Adapter.IDQueue.FairRoundRobinScheduleQueue.ActionExistsWithRetryCountGreaterThan method added.
* Decal.Adapter.IDQueue.FairIDQueue.Current_MessageProcessed method changed

### 2017-11-22
[Mag-nus]
* Strong-Named signature removed from assembly
* Decal.Adapter.IDQueue interval changed from 600ms to 10ms