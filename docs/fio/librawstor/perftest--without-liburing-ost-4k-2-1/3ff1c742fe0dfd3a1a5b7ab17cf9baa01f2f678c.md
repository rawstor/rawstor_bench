[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2025-10-14 20:53:44

refs/heads/test/asan

[3ff1c74](https://github.com/rawstor/librawstor/commit/3ff1c742fe0dfd3a1a5b7ab17cf9baa01f2f678c)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11821: Tue Oct 14 20:53:41 2025
  read: IOPS=9937, BW=38.8MiB/s (40.7MB/s)(388MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5046.56, stdev=2918.04
     lat (usec): min=29, max=31306, avg=93.35, stdev=269.86
    clat percentiles (msec):
     |  1.00th=[  207],  5.00th=[  567], 10.00th=[ 1011], 20.00th=[ 1989],
     | 30.00th=[ 2970], 40.00th=[ 3977], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=36376, max=44040, per=100.00%, avg=39755.20, stdev=2205.65, samples=20
   iops        : min= 9094, max=11010, avg=9938.80, stdev=551.41, samples=20
  write: IOPS=9927, BW=38.8MiB/s (40.7MB/s)(388MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5059.12, stdev=2928.36
     lat (usec): min=47, max=34722, avg=105.47, stdev=291.82
    clat percentiles (msec):
     |  1.00th=[  203],  5.00th=[  558], 10.00th=[ 1011], 20.00th=[ 1989],
     | 30.00th=[ 2970], 40.00th=[ 4010], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8154], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=37264, max=44360, per=100.00%, avg=39713.20, stdev=2188.06, samples=20
   iops        : min= 9316, max=11090, avg=9928.30, stdev=547.01, samples=20
  lat (msec)   : 250=1.55%, 500=2.78%, 750=2.79%, 1000=2.78%, 2000=10.21%
  lat (msec)   : >=2000=79.90%
  cpu          : usr=11.73%, sys=37.16%, ctx=103625, majf=0, minf=45
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=99388,99283,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=38.8MiB/s (40.7MB/s), 38.8MiB/s-38.8MiB/s (40.7MB/s-40.7MB/s), io=388MiB (407MB), run=10001-10001msec
  WRITE: bw=38.8MiB/s (40.7MB/s), 38.8MiB/s-38.8MiB/s (40.7MB/s-40.7MB/s), io=388MiB (407MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=1/119, sectors=208/36336, merge=0/1043, ticks=0/260, in_queue=267, util=0.21%
```
