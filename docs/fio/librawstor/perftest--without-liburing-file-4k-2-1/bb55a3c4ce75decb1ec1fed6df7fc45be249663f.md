[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2025-10-24 06:47:59

refs/heads/ci/packages

[bb55a3c](https://github.com/rawstor/librawstor/commit/bb55a3c4ce75decb1ec1fed6df7fc45be249663f)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11064: Fri Oct 24 06:47:56 2025
  read: IOPS=166k, BW=650MiB/s (681MB/s)(6499MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=110, max=10110, avg=5486.74, stdev=2734.56
     lat (nsec): min=1683, max=133450, avg=2387.59, stdev=1251.28
    clat percentiles (msec):
     |  1.00th=[  275],  5.00th=[  986], 10.00th=[ 1670], 20.00th=[ 2735],
     | 30.00th=[ 3708], 40.00th=[ 4665], 50.00th=[ 5604], 60.00th=[ 6477],
     | 70.00th=[ 7349], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=382216, max=748064, per=99.70%, avg=663386.53, stdev=116736.18, samples=19
   iops        : min=95554, max=187016, avg=165846.63, stdev=29184.05, samples=19
  write: IOPS=166k, BW=649MiB/s (681MB/s)(6494MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10110, avg=5488.25, stdev=2735.22
     lat (usec): min=4, max=183, avg= 9.12, stdev= 4.73
    clat percentiles (msec):
     |  1.00th=[  275],  5.00th=[  986], 10.00th=[ 1670], 20.00th=[ 2735],
     | 30.00th=[ 3708], 40.00th=[ 4665], 50.00th=[ 5604], 60.00th=[ 6477],
     | 70.00th=[ 7349], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10134], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=379848, max=748400, per=99.67%, avg=662690.95, stdev=116584.19, samples=19
   iops        : min=94962, max=187100, avg=165672.74, stdev=29146.05, samples=19
  lat (msec)   : 250=0.84%, 500=1.38%, 750=1.42%, 1000=1.42%, 2000=7.90%
  lat (msec)   : >=2000=87.02%
  cpu          : usr=30.00%, sys=69.97%, ctx=78, majf=0, minf=34
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1663684,1662422,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=650MiB/s (681MB/s), 650MiB/s-650MiB/s (681MB/s-681MB/s), io=6499MiB (6814MB), run=10001-10001msec
  WRITE: bw=649MiB/s (681MB/s), 649MiB/s-649MiB/s (681MB/s-681MB/s), io=6494MiB (6809MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/107, sectors=0/192960, merge=0/50, ticks=0/521, in_queue=520, util=0.17%
```
