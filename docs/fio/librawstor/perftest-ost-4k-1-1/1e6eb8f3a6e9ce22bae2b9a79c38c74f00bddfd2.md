[&lt; back](..)

# perftest-ost-4k-1-1

2026-11-18 08:46:20

refs/heads/add/object-image-import-export

[1e6eb8f](https://github.com/rawstor/librawstor/commit/1e6eb8f3a6e9ce22bae2b9a79c38c74f00bddfd2)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16263: Wed Nov 18 08:45:09 2026
  read: IOPS=28.0k, BW=109MiB/s (115MB/s)(1094MiB/10001msec)
    slat (nsec): min=841, max=32318, avg=1012.93, stdev=345.03
    clat (usec): min=27, max=214, avg=34.49, stdev= 3.77
     lat (usec): min=28, max=215, avg=35.50, stdev= 3.82
    clat percentiles (usec):
     |  1.00th=[   31],  5.00th=[   32], 10.00th=[   32], 20.00th=[   32],
     | 30.00th=[   33], 40.00th=[   34], 50.00th=[   35], 60.00th=[   35],
     | 70.00th=[   36], 80.00th=[   37], 90.00th=[   38], 95.00th=[   41],
     | 99.00th=[   49], 99.50th=[   52], 99.90th=[   60], 99.95th=[   68],
     | 99.99th=[  103]
   bw (  KiB/s): min=106872, max=117256, per=100.00%, avg=112123.05, stdev=2972.93, samples=20
   iops        : min=26718, max=29314, avg=28030.70, stdev=743.16, samples=20
  lat (usec)   : 50=99.24%, 100=0.74%, 250=0.01%
  cpu          : usr=13.36%, sys=34.38%, ctx=280192, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=280188,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16264: Wed Nov 18 08:45:09 2026
  write: IOPS=2909, BW=11.4MiB/s (11.9MB/s)(114MiB/10001msec); 0 zone resets
    slat (nsec): min=1913, max=107582, avg=2432.37, stdev=1118.78
    clat (usec): min=241, max=14780, avg=340.96, stdev=151.37
     lat (usec): min=243, max=14783, avg=343.39, stdev=151.50
    clat percentiles (usec):
     |  1.00th=[  260],  5.00th=[  269], 10.00th=[  281], 20.00th=[  293],
     | 30.00th=[  306], 40.00th=[  318], 50.00th=[  326], 60.00th=[  334],
     | 70.00th=[  343], 80.00th=[  355], 90.00th=[  379], 95.00th=[  433],
     | 99.00th=[  766], 99.50th=[  922], 99.90th=[ 1811], 99.95th=[ 2147],
     | 99.99th=[ 7046]
   bw (  KiB/s): min=10512, max=12216, per=100.00%, avg=11642.20, stdev=442.15, samples=20
   iops        : min= 2628, max= 3054, avg=2910.45, stdev=110.54, samples=20
  lat (usec)   : 250=0.18%, 500=96.32%, 750=2.46%, 1000=0.65%
  lat (msec)   : 2=0.34%, 4=0.05%, 10=0.01%, 20=0.01%
  cpu          : usr=1.79%, sys=3.79%, ctx=29096, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,29096,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=109MiB/s (115MB/s), 109MiB/s-109MiB/s (115MB/s-115MB/s), io=1094MiB (1148MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=11.4MiB/s (11.9MB/s), 11.4MiB/s-11.4MiB/s (11.9MB/s-11.9MB/s), io=114MiB (119MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=2/74519, sectors=16/1666944, merge=0/112319, ticks=5/17853, in_queue=17858, util=36.10%
```
