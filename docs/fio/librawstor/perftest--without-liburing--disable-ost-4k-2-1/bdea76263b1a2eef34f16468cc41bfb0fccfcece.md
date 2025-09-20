[&lt; back](..)

# perftest--without-liburing--disable-ost-4k-2-1

2025-09-20 21:51:14

refs/heads/add/cppringbuf

[bdea762](https://github.com/rawstor/librawstor/commit/bdea76263b1a2eef34f16468cc41bfb0fccfcece)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10373: Sat Sep 20 21:51:12 2025
  read: IOPS=169k, BW=658MiB/s (690MB/s)(6584MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10110, avg=5523.47, stdev=2732.60
     lat (nsec): min=1632, max=101900, avg=2348.65, stdev=1276.06
    clat percentiles (msec):
     |  1.00th=[  288],  5.00th=[ 1011], 10.00th=[ 1703], 20.00th=[ 2769],
     | 30.00th=[ 3775], 40.00th=[ 4732], 50.00th=[ 5604], 60.00th=[ 6544],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10134], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=362304, max=758480, per=99.48%, avg=670672.00, stdev=124403.65, samples=19
   iops        : min=90576, max=189620, avg=167668.00, stdev=31100.91, samples=19
  write: IOPS=168k, BW=658MiB/s (690MB/s)(6579MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10110, avg=5524.76, stdev=2733.08
     lat (usec): min=4, max=143, avg= 8.98, stdev= 4.78
    clat percentiles (msec):
     |  1.00th=[  288],  5.00th=[ 1011], 10.00th=[ 1703], 20.00th=[ 2769],
     | 30.00th=[ 3775], 40.00th=[ 4732], 50.00th=[ 5604], 60.00th=[ 6544],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10134], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=362168, max=754672, per=99.46%, avg=669982.74, stdev=124262.68, samples=19
   iops        : min=90542, max=188668, avg=167495.68, stdev=31065.68, samples=19
  lat (msec)   : 250=0.78%, 500=1.47%, 750=1.37%, 1000=1.33%, 2000=7.72%
  lat (msec)   : >=2000=87.33%
  cpu          : usr=27.05%, sys=72.92%, ctx=64, majf=0, minf=35
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1685561,1684211,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=658MiB/s (690MB/s), 658MiB/s-658MiB/s (690MB/s-690MB/s), io=6584MiB (6904MB), run=10001-10001msec
  WRITE: bw=658MiB/s (690MB/s), 658MiB/s-658MiB/s (690MB/s-690MB/s), io=6579MiB (6899MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/11, sectors=0/2888, merge=0/54, ticks=0/11, in_queue=11, util=0.01%
```
