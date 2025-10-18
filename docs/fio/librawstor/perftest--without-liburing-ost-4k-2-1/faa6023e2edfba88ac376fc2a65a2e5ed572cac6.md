[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2025-10-18 20:38:55

refs/heads/test/asan

[faa6023](https://github.com/rawstor/librawstor/commit/faa6023e2edfba88ac376fc2a65a2e5ed572cac6)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11759: Sat Oct 18 20:38:53 2025
  read: IOPS=9427, BW=36.8MiB/s (38.6MB/s)(368MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10110, avg=4987.98, stdev=2919.90
     lat (usec): min=30, max=29597, avg=98.04, stdev=245.62
    clat percentiles (msec):
     |  1.00th=[  209],  5.00th=[  567], 10.00th=[ 1003], 20.00th=[ 1888],
     | 30.00th=[ 2903], 40.00th=[ 3943], 50.00th=[ 4933], 60.00th=[ 5940],
     | 70.00th=[ 7013], 80.00th=[ 8020], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=34480, max=42704, per=100.00%, avg=37830.32, stdev=2399.11, samples=19
   iops        : min= 8620, max=10676, avg=9457.58, stdev=599.78, samples=19
  write: IOPS=9397, BW=36.7MiB/s (38.5MB/s)(367MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10110, avg=4990.69, stdev=2926.17
     lat (usec): min=53, max=28919, avg=111.88, stdev=271.43
    clat percentiles (msec):
     |  1.00th=[  203],  5.00th=[  558], 10.00th=[ 1003], 20.00th=[ 1888],
     | 30.00th=[ 2903], 40.00th=[ 3910], 50.00th=[ 4933], 60.00th=[ 6007],
     | 70.00th=[ 7013], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=34824, max=42320, per=100.00%, avg=37721.68, stdev=2433.09, samples=19
   iops        : min= 8706, max=10580, avg=9430.42, stdev=608.27, samples=19
  lat (msec)   : 250=1.51%, 500=2.79%, 750=2.88%, 1000=2.79%, 2000=11.27%
  lat (msec)   : >=2000=78.76%
  cpu          : usr=12.78%, sys=36.13%, ctx=101375, majf=0, minf=41
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=94288,93989,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=36.8MiB/s (38.6MB/s), 36.8MiB/s-36.8MiB/s (38.6MB/s-38.6MB/s), io=368MiB (386MB), run=10001-10001msec
  WRITE: bw=36.7MiB/s (38.5MB/s), 36.7MiB/s-36.7MiB/s (38.5MB/s-38.5MB/s), io=367MiB (385MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/123, sectors=0/37848, merge=0/1017, ticks=0/125, in_queue=131, util=0.20%
```
