[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2026-03-25 08:44:39

refs/heads/fix/breakmshot

[1bee1dd](https://github.com/rawstor/librawstor/commit/1bee1dde6e18056b0eebe14ea59f695d43bfca5d)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=12343: Wed Mar 25 08:44:11 2026
  read: IOPS=9638, BW=37.6MiB/s (39.5MB/s)(377MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10110, avg=5080.63, stdev=2899.59
     lat (usec): min=151, max=18389, avg=206.52, stdev=151.03
    clat percentiles (msec):
     |  1.00th=[  224],  5.00th=[  584], 10.00th=[ 1062], 20.00th=[ 2072],
     | 30.00th=[ 3071], 40.00th=[ 4044], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=36952, max=41306, per=99.90%, avg=38516.00, stdev=977.78, samples=19
   iops        : min= 9238, max=10326, avg=9628.84, stdev=244.37, samples=19
  lat (msec)   : 250=1.26%, 500=2.79%, 750=2.79%, 1000=2.56%, 2000=9.95%
  lat (msec)   : >=2000=80.63%
  cpu          : usr=17.53%, sys=59.49%, ctx=48424, majf=0, minf=1690540
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=96394,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=12354: Wed Mar 25 08:44:11 2026
  write: IOPS=8289, BW=32.4MiB/s (34.0MB/s)(324MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=10320, max=20319, avg=15230.50, stdev=2886.39
     lat (usec): min=175, max=19765, avg=240.17, stdev=202.80
    clat percentiles (msec):
     |  1.00th=[10402],  5.00th=[10805], 10.00th=[11342], 20.00th=[12281],
     | 30.00th=[13221], 40.00th=[14160], 50.00th=[15100], 60.00th=[16174],
     | 70.00th=[17113], 80.00th=[17113], 90.00th=[17113], 95.00th=[17113],
     | 99.00th=[17113], 99.50th=[17113], 99.90th=[17113], 99.95th=[17113],
     | 99.99th=[17113]
   bw (  KiB/s): min=30960, max=36784, per=100.00%, avg=33160.00, stdev=1653.62, samples=20
   iops        : min= 7740, max= 9196, avg=8290.00, stdev=413.40, samples=20
  lat (msec)   : >=2000=100.00%
  cpu          : usr=15.43%, sys=53.09%, ctx=41924, majf=0, minf=1475979
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,82900,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=37.6MiB/s (39.5MB/s), 37.6MiB/s-37.6MiB/s (39.5MB/s-39.5MB/s), io=377MiB (395MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=32.4MiB/s (34.0MB/s), 32.4MiB/s-32.4MiB/s (34.0MB/s-34.0MB/s), io=324MiB (340MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/55197, sectors=0/722976, merge=0/1600, ticks=0/202908, in_queue=202912, util=11.91%
```
