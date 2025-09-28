[&lt; back](..)

# perftest--disable-ost-4k-2-1

2025-09-28 20:08:52

refs/heads/add/socket

[5dded36](https://github.com/rawstor/librawstor/commit/5dded36e9d4baaed3055c2d7bddf2e03e51fd1da)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10515: Sun Sep 28 20:08:50 2025
  read: IOPS=70.8k, BW=276MiB/s (290MB/s)(2764MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5356.15, stdev=2789.93
     lat (nsec): min=1343, max=126046, avg=5242.57, stdev=3919.95
    clat percentiles (msec):
     |  1.00th=[  228],  5.00th=[  726], 10.00th=[ 1401], 20.00th=[ 2601],
     | 30.00th=[ 3540], 40.00th=[ 4463], 50.00th=[ 5403], 60.00th=[ 6342],
     | 70.00th=[ 7282], 80.00th=[ 8221], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=207072, max=319720, per=99.66%, avg=282064.84, stdev=36987.03, samples=19
   iops        : min=51768, max=79930, avg=70516.21, stdev=9246.76, samples=19
  write: IOPS=70.6k, BW=276MiB/s (289MB/s)(2760MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5353.37, stdev=2788.62
     lat (usec): min=3, max=830, avg=22.09, stdev= 6.85
    clat percentiles (msec):
     |  1.00th=[  226],  5.00th=[  718], 10.00th=[ 1418], 20.00th=[ 2567],
     | 30.00th=[ 3540], 40.00th=[ 4463], 50.00th=[ 5403], 60.00th=[ 6342],
     | 70.00th=[ 7282], 80.00th=[ 8221], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=204448, max=321192, per=99.70%, avg=281725.05, stdev=37231.73, samples=19
   iops        : min=51112, max=80298, avg=70431.26, stdev=9307.93, samples=19
  lat (msec)   : 250=1.23%, 500=2.08%, 750=1.92%, 1000=1.81%, 2000=7.30%
  lat (msec)   : >=2000=85.66%
  cpu          : usr=17.78%, sys=50.92%, ctx=289877, majf=0, minf=32
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=707654,706480,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=276MiB/s (290MB/s), 276MiB/s-276MiB/s (290MB/s-290MB/s), io=2764MiB (2899MB), run=10001-10001msec
  WRITE: bw=276MiB/s (289MB/s), 276MiB/s-276MiB/s (289MB/s-289MB/s), io=2760MiB (2894MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=1/21, sectors=144/9416, merge=0/73, ticks=1/21, in_queue=22, util=0.02%
```
