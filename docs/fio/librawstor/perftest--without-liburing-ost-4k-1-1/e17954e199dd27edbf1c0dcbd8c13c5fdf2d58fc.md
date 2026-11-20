[&lt; back](..)

# perftest--without-liburing-ost-4k-1-1

2026-11-20 11:26:39

refs/heads/main

[e17954e](https://github.com/rawstor/librawstor/commit/e17954e199dd27edbf1c0dcbd8c13c5fdf2d58fc)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16305: Fri Nov 20 11:25:54 2026
  read: IOPS=17.5k, BW=68.2MiB/s (71.5MB/s)(682MiB/10001msec)
    slat (nsec): min=1382, max=43003, avg=2076.51, stdev=879.98
    clat (usec): min=43, max=839, avg=54.65, stdev=10.34
     lat (usec): min=44, max=844, avg=56.73, stdev=10.65
    clat percentiles (usec):
     |  1.00th=[   45],  5.00th=[   46], 10.00th=[   46], 20.00th=[   47],
     | 30.00th=[   48], 40.00th=[   49], 50.00th=[   51], 60.00th=[   57],
     | 70.00th=[   60], 80.00th=[   63], 90.00th=[   67], 95.00th=[   72],
     | 99.00th=[   83], 99.50th=[   86], 99.90th=[   97], 99.95th=[  114],
     | 99.99th=[  359]
   bw (  KiB/s): min=62136, max=77226, per=100.00%, avg=69877.00, stdev=4344.91, samples=20
   iops        : min=15534, max=19306, avg=17469.15, stdev=1086.12, samples=20
  lat (usec)   : 50=45.93%, 100=53.99%, 250=0.06%, 500=0.01%, 750=0.01%
  lat (usec)   : 1000=0.01%
  cpu          : usr=16.74%, sys=25.90%, ctx=174616, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=174611,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16307: Fri Nov 20 11:25:54 2026
  write: IOPS=2440, BW=9762KiB/s (9997kB/s)(95.3MiB/10001msec); 0 zone resets
    slat (nsec): min=3655, max=27370, avg=5741.27, stdev=1601.04
    clat (usec): min=238, max=156940, avg=402.88, stdev=1762.42
     lat (usec): min=243, max=156945, avg=408.63, stdev=1762.43
    clat percentiles (usec):
     |  1.00th=[   260],  5.00th=[   273], 10.00th=[   281], 20.00th=[   302],
     | 30.00th=[   318], 40.00th=[   330], 50.00th=[   343], 60.00th=[   351],
     | 70.00th=[   363], 80.00th=[   375], 90.00th=[   400], 95.00th=[   433],
     | 99.00th=[  1237], 99.50th=[  2278], 99.90th=[ 10945], 99.95th=[ 14353],
     | 99.99th=[135267]
   bw (  KiB/s): min= 4920, max=11160, per=100.00%, avg=9766.35, stdev=1571.80, samples=20
   iops        : min= 1230, max= 2790, avg=2441.55, stdev=392.95, samples=20
  lat (usec)   : 250=0.18%, 500=97.04%, 750=1.23%, 1000=0.29%
  lat (msec)   : 2=0.71%, 4=0.23%, 10=0.20%, 20=0.09%, 50=0.01%
  lat (msec)   : 100=0.01%, 250=0.01%
  cpu          : usr=4.02%, sys=4.43%, ctx=24411, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,24408,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=68.2MiB/s (71.5MB/s), 68.2MiB/s-68.2MiB/s (71.5MB/s-71.5MB/s), io=682MiB (715MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=9762KiB/s (9997kB/s), 9762KiB/s-9762KiB/s (9997kB/s-9997kB/s), io=95.3MiB (100.0MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=1/62611, sectors=8/1454912, merge=0/94405, ticks=0/20687, in_queue=20689, util=33.97%
```
