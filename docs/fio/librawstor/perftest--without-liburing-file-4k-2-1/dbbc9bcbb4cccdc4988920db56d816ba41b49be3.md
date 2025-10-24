[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2025-10-24 07:30:58

refs/heads/ci/packages

[dbbc9bc](https://github.com/rawstor/librawstor/commit/dbbc9bcbb4cccdc4988920db56d816ba41b49be3)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11021: Fri Oct 24 07:30:55 2025
  read: IOPS=235k, BW=919MiB/s (963MB/s)(9186MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=103, max=10103, avg=5384.37, stdev=2753.55
     lat (nsec): min=996, max=235209, avg=1721.24, stdev=930.29
    clat percentiles (msec):
     |  1.00th=[  259],  5.00th=[  969], 10.00th=[ 1569], 20.00th=[ 2601],
     | 30.00th=[ 3574], 40.00th=[ 4530], 50.00th=[ 5403], 60.00th=[ 6342],
     | 70.00th=[ 7282], 80.00th=[ 8221], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=556264, max=1028552, per=100.00%, avg=940660.40, stdev=138508.96, samples=20
   iops        : min=139066, max=257138, avg=235165.20, stdev=34627.30, samples=20
  write: IOPS=235k, BW=918MiB/s (963MB/s)(9181MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=103, max=10103, avg=5386.42, stdev=2754.50
     lat (usec): min=3, max=243, avg= 6.30, stdev= 3.45
    clat percentiles (msec):
     |  1.00th=[  259],  5.00th=[  969], 10.00th=[ 1569], 20.00th=[ 2601],
     | 30.00th=[ 3574], 40.00th=[ 4530], 50.00th=[ 5403], 60.00th=[ 6342],
     | 70.00th=[ 7282], 80.00th=[ 8221], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=553344, max=1021752, per=100.00%, avg=940084.00, stdev=138254.60, samples=20
   iops        : min=138336, max=255438, avg=235021.00, stdev=34563.65, samples=20
  lat (msec)   : 250=0.94%, 500=1.47%, 750=1.29%, 1000=1.50%, 2000=8.86%
  lat (msec)   : >=2000=85.93%
  cpu          : usr=36.18%, sys=63.80%, ctx=72, majf=0, minf=38
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=2351652,2350210,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=919MiB/s (963MB/s), 919MiB/s-919MiB/s (963MB/s-963MB/s), io=9186MiB (9632MB), run=10001-10001msec
  WRITE: bw=918MiB/s (963MB/s), 918MiB/s-918MiB/s (963MB/s-963MB/s), io=9181MiB (9626MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/143, sectors=0/11352, merge=0/284, ticks=0/174, in_queue=173, util=0.05%
```
