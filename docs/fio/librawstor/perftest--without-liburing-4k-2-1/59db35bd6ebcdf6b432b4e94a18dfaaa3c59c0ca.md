[&lt; back](..)

# perftest--without-liburing-4k-2-1

2025-09-28 19:24:46

refs/heads/add/socket

[59db35b](https://github.com/rawstor/librawstor/commit/59db35bd6ebcdf6b432b4e94a18dfaaa3c59c0ca)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11564: Sun Sep 28 19:24:44 2025
  read: IOPS=10.3k, BW=40.1MiB/s (42.0MB/s)(401MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5034.60, stdev=2908.06
     lat (usec): min=29, max=30030, avg=90.92, stdev=269.79
    clat percentiles (msec):
     |  1.00th=[  218],  5.00th=[  600], 10.00th=[ 1036], 20.00th=[ 1972],
     | 30.00th=[ 2970], 40.00th=[ 3977], 50.00th=[ 5000], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=38680, max=46312, per=100.00%, avg=41034.80, stdev=2147.51, samples=20
   iops        : min= 9670, max=11578, avg=10258.70, stdev=536.88, samples=20
  write: IOPS=10.2k, BW=40.0MiB/s (41.9MB/s)(400MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5043.77, stdev=2915.55
     lat (usec): min=49, max=32605, avg=101.84, stdev=253.63
    clat percentiles (msec):
     |  1.00th=[  211],  5.00th=[  592], 10.00th=[ 1036], 20.00th=[ 1972],
     | 30.00th=[ 2970], 40.00th=[ 3977], 50.00th=[ 5000], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=38464, max=45536, per=100.00%, avg=40969.60, stdev=1979.31, samples=20
   iops        : min= 9616, max=11384, avg=10242.40, stdev=494.83, samples=20
  lat (msec)   : 250=1.37%, 500=2.58%, 750=2.83%, 1000=2.83%, 2000=10.73%
  lat (msec)   : >=2000=79.65%
  cpu          : usr=11.02%, sys=37.26%, ctx=106664, majf=0, minf=304
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=102587,102424,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=40.1MiB/s (42.0MB/s), 40.1MiB/s-40.1MiB/s (42.0MB/s-42.0MB/s), io=401MiB (420MB), run=10001-10001msec
  WRITE: bw=40.0MiB/s (41.9MB/s), 40.0MiB/s-40.0MiB/s (41.9MB/s-41.9MB/s), io=400MiB (420MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/289, sectors=0/46344, merge=0/1429, ticks=0/448, in_queue=452, util=0.20%
```
