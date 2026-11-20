[&lt; back](..)

# perftest--without-liburing-ost-4k-2-1

2026-11-20 10:30:46

refs/heads/add/list-by-location

[a23f3a5](https://github.com/rawstor/librawstor/commit/a23f3a5bf1aec5777cdd731d4bfbfe89e85fdd79)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16303: Fri Nov 20 10:29:47 2026
  read: IOPS=30.9k, BW=121MiB/s (127MB/s)(1208MiB/10001msec)
    slat (nsec): min=307, max=50309, avg=1822.12, stdev=894.57
    clat (usec): min=24, max=1408, avg=62.45, stdev=14.28
     lat (usec): min=26, max=1410, avg=64.27, stdev=14.09
    clat percentiles (usec):
     |  1.00th=[   34],  5.00th=[   43], 10.00th=[   47], 20.00th=[   51],
     | 30.00th=[   54], 40.00th=[   59], 50.00th=[   62], 60.00th=[   66],
     | 70.00th=[   71], 80.00th=[   75], 90.00th=[   80], 95.00th=[   85],
     | 99.00th=[   96], 99.50th=[  101], 99.90th=[  121], 99.95th=[  135],
     | 99.99th=[  172]
   bw (  KiB/s): min=113304, max=143624, per=100.00%, avg=123814.30, stdev=7308.95, samples=20
   iops        : min=28326, max=35906, avg=30953.50, stdev=1827.24, samples=20
  lat (usec)   : 50=18.68%, 100=80.77%, 250=0.55%, 500=0.01%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%
  cpu          : usr=28.66%, sys=27.45%, ctx=156447, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=309363,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16306: Fri Nov 20 10:29:47 2026
  write: IOPS=2145, BW=8583KiB/s (8789kB/s)(83.8MiB/10001msec); 0 zone resets
    slat (nsec): min=607, max=40375, avg=5053.46, stdev=2944.33
    clat (usec): min=402, max=26865, avg=926.25, stdev=523.74
     lat (usec): min=405, max=26866, avg=931.30, stdev=523.60
    clat percentiles (usec):
     |  1.00th=[  469],  5.00th=[  519], 10.00th=[  553], 20.00th=[  635],
     | 30.00th=[  717], 40.00th=[  832], 50.00th=[  971], 60.00th=[ 1029],
     | 70.00th=[ 1074], 80.00th=[ 1123], 90.00th=[ 1205], 95.00th=[ 1287],
     | 99.00th=[ 1696], 99.50th=[ 1860], 99.90th=[ 3949], 99.95th=[11600],
     | 99.99th=[21890]
   bw (  KiB/s): min= 7776, max= 9264, per=100.00%, avg=8586.55, stdev=417.20, samples=20
   iops        : min= 1944, max= 2316, avg=2146.60, stdev=104.28, samples=20
  lat (usec)   : 500=3.22%, 750=30.62%, 1000=21.04%
  lat (msec)   : 2=44.80%, 4=0.22%, 10=0.04%, 20=0.04%, 50=0.02%
  cpu          : usr=3.36%, sys=2.50%, ctx=16867, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,21458,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=121MiB/s (127MB/s), 121MiB/s-121MiB/s (127MB/s-127MB/s), io=1208MiB (1267MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=8583KiB/s (8789kB/s), 8583KiB/s-8583KiB/s (8789kB/s-8789kB/s), io=83.8MiB (87.9MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=0/52334, sectors=0/1217176, merge=0/77724, ticks=0/19594, in_queue=19596, util=38.35%
```
