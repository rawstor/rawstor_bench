[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2025-10-19 09:56:34

refs/heads/feat/ci

[c4cda52](https://github.com/rawstor/librawstor/commit/c4cda52e7bbeebda8a218aede54afbaf883daef3)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10910: Sun Oct 19 09:56:32 2025
  read: IOPS=171k, BW=667MiB/s (699MB/s)(6672MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10111, avg=5486.94, stdev=2742.23
     lat (nsec): min=1673, max=198260, avg=2342.58, stdev=1154.41
    clat percentiles (msec):
     |  1.00th=[  275],  5.00th=[  978], 10.00th=[ 1670], 20.00th=[ 2735],
     | 30.00th=[ 3708], 40.00th=[ 4665], 50.00th=[ 5537], 60.00th=[ 6477],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=383464, max=755048, per=99.53%, avg=679877.89, stdev=117872.53, samples=19
   iops        : min=95866, max=188762, avg=169969.47, stdev=29468.13, samples=19
  write: IOPS=171k, BW=667MiB/s (699MB/s)(6666MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10111, avg=5488.28, stdev=2742.72
     lat (usec): min=4, max=119, avg= 8.85, stdev= 4.54
    clat percentiles (msec):
     |  1.00th=[  275],  5.00th=[  978], 10.00th=[ 1670], 20.00th=[ 2735],
     | 30.00th=[ 3708], 40.00th=[ 4665], 50.00th=[ 5537], 60.00th=[ 6477],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=384064, max=757232, per=99.52%, avg=679317.05, stdev=117812.21, samples=19
   iops        : min=96016, max=189308, avg=169829.26, stdev=29453.05, samples=19
  lat (msec)   : 250=0.85%, 500=1.47%, 750=1.42%, 1000=1.39%, 2000=7.90%
  lat (msec)   : >=2000=86.97%
  cpu          : usr=29.38%, sys=70.60%, ctx=62, majf=0, minf=35
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1707907,1706571,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=667MiB/s (699MB/s), 667MiB/s-667MiB/s (699MB/s-699MB/s), io=6672MiB (6996MB), run=10001-10001msec
  WRITE: bw=667MiB/s (699MB/s), 667MiB/s-667MiB/s (699MB/s-699MB/s), io=6666MiB (6990MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/13, sectors=0/1880, merge=0/21, ticks=0/9, in_queue=8, util=0.03%
```
