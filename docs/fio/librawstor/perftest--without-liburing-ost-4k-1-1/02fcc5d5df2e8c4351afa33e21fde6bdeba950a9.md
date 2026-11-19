[&lt; back](..)

# perftest--without-liburing-ost-4k-1-1

2026-11-19 18:17:11

refs/heads/add/location-list

[02fcc5d](https://github.com/rawstor/librawstor/commit/02fcc5d5df2e8c4351afa33e21fde6bdeba950a9)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16545: Thu Nov 19 18:16:49 2026
  read: IOPS=9553, BW=37.3MiB/s (39.1MB/s)(373MiB/10001msec)
    slat (nsec): min=3216, max=39544, avg=4640.79, stdev=1636.01
    clat (usec): min=75, max=598, avg=98.64, stdev=13.23
     lat (usec): min=79, max=604, avg=103.28, stdev=13.89
    clat percentiles (usec):
     |  1.00th=[   79],  5.00th=[   81], 10.00th=[   82], 20.00th=[   85],
     | 30.00th=[   88], 40.00th=[   97], 50.00th=[  102], 60.00th=[  103],
     | 70.00th=[  105], 80.00th=[  108], 90.00th=[  114], 95.00th=[  123],
     | 99.00th=[  135], 99.50th=[  137], 99.90th=[  149], 99.95th=[  155],
     | 99.99th=[  172]
   bw (  KiB/s): min=35080, max=43720, per=100.00%, avg=38233.75, stdev=2526.42, samples=20
   iops        : min= 8770, max=10930, avg=9558.35, stdev=631.65, samples=20
  lat (usec)   : 100=43.74%, 250=56.26%, 500=0.01%, 750=0.01%
  cpu          : usr=20.55%, sys=24.91%, ctx=95554, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=95544,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16547: Thu Nov 19 18:16:49 2026
  write: IOPS=2108, BW=8434KiB/s (8637kB/s)(82.4MiB/10001msec); 0 zone resets
    slat (nsec): min=7865, max=40526, avg=10073.13, stdev=2454.98
    clat (usec): min=326, max=9958, avg=462.45, stdev=171.09
     lat (usec): min=335, max=9966, avg=472.52, stdev=171.16
    clat percentiles (usec):
     |  1.00th=[  347],  5.00th=[  363], 10.00th=[  371], 20.00th=[  396],
     | 30.00th=[  412], 40.00th=[  429], 50.00th=[  441], 60.00th=[  457],
     | 70.00th=[  474], 80.00th=[  494], 90.00th=[  537], 95.00th=[  594],
     | 99.00th=[  898], 99.50th=[ 1303], 99.90th=[ 2212], 99.95th=[ 3687],
     | 99.99th=[ 5473]
   bw (  KiB/s): min= 7334, max= 8976, per=100.00%, avg=8438.00, stdev=392.00, samples=20
   iops        : min= 1833, max= 2244, avg=2109.45, stdev=98.05, samples=20
  lat (usec)   : 500=81.56%, 750=16.75%, 1000=0.93%
  lat (msec)   : 2=0.59%, 4=0.12%, 10=0.04%
  cpu          : usr=6.02%, sys=5.82%, ctx=21088, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,21088,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=37.3MiB/s (39.1MB/s), 37.3MiB/s-37.3MiB/s (39.1MB/s-39.1MB/s), io=373MiB (391MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=8434KiB/s (8637kB/s), 8434KiB/s-8434KiB/s (8637kB/s-8637kB/s), io=82.4MiB (86.4MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=1/53523, sectors=8/1265080, merge=0/81163, ticks=4/7909, in_queue=7912, util=28.24%
```
