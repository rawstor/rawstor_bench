[&lt; back](..)

# perftest-file-4k-2-1

2026-09-14 09:59:18

refs/heads/releases/v0.2.11

[92a0dad](https://github.com/rawstor/librawstor/commit/92a0dad8ff4c5c4fc05b7cfbdf1239e8e4f362fe)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=13972: Mon Sep 14 09:58:09 2026
  read: IOPS=599k, BW=2340MiB/s (2454MB/s)(22.9GiB/10001msec)
    slat (nsec): min=152, max=35863, avg=176.87, stdev=115.08
    clat (nsec): min=2215, max=96773, avg=2953.94, stdev=543.37
     lat (nsec): min=2388, max=96976, avg=3130.81, stdev=559.28
    clat percentiles (nsec):
     |  1.00th=[ 2544],  5.00th=[ 2608], 10.00th=[ 2672], 20.00th=[ 2736],
     | 30.00th=[ 2768], 40.00th=[ 2832], 50.00th=[ 2896], 60.00th=[ 2960],
     | 70.00th=[ 3024], 80.00th=[ 3120], 90.00th=[ 3248], 95.00th=[ 3376],
     | 99.00th=[ 3696], 99.50th=[ 4048], 99.90th=[10816], 99.95th=[11456],
     | 99.99th=[15936]
   bw (  MiB/s): min= 2323, max= 2373, per=100.00%, avg=2341.54, stdev=12.94, samples=20
   iops        : min=594700, max=607488, avg=599435.70, stdev=3313.33, samples=20
  lat (usec)   : 4=99.48%, 10=0.24%, 20=0.27%, 50=0.01%, 100=0.01%
  cpu          : usr=38.97%, sys=61.01%, ctx=65, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=5991364,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=13973: Mon Sep 14 09:58:09 2026
  write: IOPS=76.5k, BW=299MiB/s (313MB/s)(2990MiB/10001msec); 0 zone resets
    slat (nsec): min=226, max=119417, avg=509.11, stdev=697.75
    clat (usec): min=3, max=3046, avg=24.99, stdev=11.50
     lat (usec): min=3, max=3047, avg=25.50, stdev=11.53
    clat percentiles (usec):
     |  1.00th=[   21],  5.00th=[   22], 10.00th=[   22], 20.00th=[   23],
     | 30.00th=[   24], 40.00th=[   24], 50.00th=[   24], 60.00th=[   25],
     | 70.00th=[   26], 80.00th=[   27], 90.00th=[   30], 95.00th=[   32],
     | 99.00th=[   39], 99.50th=[   42], 99.90th=[   64], 99.95th=[   96],
     | 99.99th=[  343]
   bw (  KiB/s): min=  448, max=339863, per=95.29%, avg=291705.14, stdev=68424.59, samples=21
   iops        : min=  112, max=84965, avg=72926.19, stdev=17106.12, samples=21
  lat (usec)   : 4=0.01%, 10=0.14%, 20=0.60%, 50=99.05%, 100=0.15%
  lat (usec)   : 250=0.03%, 500=0.01%, 750=0.01%, 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%
  cpu          : usr=16.53%, sys=25.54%, ctx=382504, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,765345,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=2340MiB/s (2454MB/s), 2340MiB/s-2340MiB/s (2454MB/s-2454MB/s), io=22.9GiB (24.5GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=299MiB/s (313MB/s), 299MiB/s-299MiB/s (313MB/s-313MB/s), io=2990MiB (3135MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/516, sectors=0/385744, merge=0/1791, ticks=0/840, in_queue=840, util=0.17%
```
