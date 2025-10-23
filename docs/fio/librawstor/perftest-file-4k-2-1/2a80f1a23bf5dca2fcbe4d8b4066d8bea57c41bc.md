[&lt; back](..)

# perftest-file-4k-2-1

2025-10-23 21:01:31

refs/heads/ci/packages

[2a80f1a](https://github.com/rawstor/librawstor/commit/2a80f1a23bf5dca2fcbe4d8b4066d8bea57c41bc)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10856: Thu Oct 23 21:01:29 2025
  read: IOPS=69.3k, BW=271MiB/s (284MB/s)(2707MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10111, avg=5386.84, stdev=2834.01
     lat (nsec): min=1423, max=172222, avg=5334.04, stdev=3783.02
    clat percentiles (msec):
     |  1.00th=[  230],  5.00th=[  726], 10.00th=[ 1334], 20.00th=[ 2534],
     | 30.00th=[ 3540], 40.00th=[ 4530], 50.00th=[ 5470], 60.00th=[ 6409],
     | 70.00th=[ 7349], 80.00th=[ 8356], 90.00th=[ 9194], 95.00th=[ 9731],
     | 99.00th=[10000], 99.50th=[10134], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=221048, max=327960, per=100.00%, avg=277217.60, stdev=31115.17, samples=20
   iops        : min=55262, max=81990, avg=69304.40, stdev=7778.79, samples=20
  write: IOPS=69.2k, BW=270MiB/s (283MB/s)(2704MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10111, avg=5385.67, stdev=2833.62
     lat (usec): min=3, max=707, avg=22.52, stdev= 6.81
    clat percentiles (msec):
     |  1.00th=[  230],  5.00th=[  726], 10.00th=[ 1351], 20.00th=[ 2534],
     | 30.00th=[ 3540], 40.00th=[ 4530], 50.00th=[ 5470], 60.00th=[ 6409],
     | 70.00th=[ 7349], 80.00th=[ 8356], 90.00th=[ 9194], 95.00th=[ 9731],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=221472, max=326608, per=100.00%, avg=276861.20, stdev=30870.54, samples=20
   iops        : min=55368, max=81652, avg=69215.30, stdev=7717.64, samples=20
  lat (msec)   : 250=1.16%, 500=2.00%, 750=2.09%, 1000=1.99%, 2000=8.00%
  lat (msec)   : >=2000=84.76%
  cpu          : usr=19.58%, sys=49.67%, ctx=279939, majf=0, minf=21
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=693044,692153,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=271MiB/s (284MB/s), 271MiB/s-271MiB/s (284MB/s-284MB/s), io=2707MiB (2839MB), run=10001-10001msec
  WRITE: bw=270MiB/s (283MB/s), 270MiB/s-270MiB/s (283MB/s-283MB/s), io=2704MiB (2835MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/30, sectors=0/9424, merge=0/55, ticks=0/22, in_queue=22, util=0.02%
```
