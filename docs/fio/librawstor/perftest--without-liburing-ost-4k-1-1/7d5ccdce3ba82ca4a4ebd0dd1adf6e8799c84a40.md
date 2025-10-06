[&lt; back](..)

# perftest--without-liburing-ost-4k-1-1

2025-10-06 09:57:17

refs/heads/add/uri

[7d5ccdc](https://github.com/rawstor/librawstor/commit/7d5ccdce3ba82ca4a4ebd0dd1adf6e8799c84a40)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11834: Mon Oct  6 09:57:15 2025
  read: IOPS=5730, BW=22.4MiB/s (23.5MB/s)(224MiB/10001msec)
    slat (nsec): min=20, max=19987, avg=184.99, stdev=251.79
    clat (usec): min=41, max=26658, avg=73.47, stdev=179.24
     lat (usec): min=41, max=26658, avg=73.66, stdev=179.25
    clat percentiles (usec):
     |  1.00th=[   54],  5.00th=[   58], 10.00th=[   61], 20.00th=[   64],
     | 30.00th=[   67], 40.00th=[   69], 50.00th=[   72], 60.00th=[   74],
     | 70.00th=[   76], 80.00th=[   80], 90.00th=[   85], 95.00th=[   92],
     | 99.00th=[  106], 99.50th=[  114], 99.90th=[  133], 99.95th=[  161],
     | 99.99th=[ 2057]
   bw (  KiB/s): min=20616, max=24576, per=100.00%, avg=22924.00, stdev=1103.89, samples=20
   iops        : min= 5154, max= 6144, avg=5731.00, stdev=275.97, samples=20
  write: IOPS=5706, BW=22.3MiB/s (23.4MB/s)(223MiB/10001msec); 0 zone resets
    slat (nsec): min=70, max=18234, avg=272.26, stdev=247.96
    clat (usec): min=56, max=30415, avg=97.57, stdev=236.91
     lat (usec): min=56, max=30415, avg=97.84, stdev=236.91
    clat percentiles (usec):
     |  1.00th=[   76],  5.00th=[   81], 10.00th=[   83], 20.00th=[   87],
     | 30.00th=[   90], 40.00th=[   93], 50.00th=[   95], 60.00th=[   97],
     | 70.00th=[  100], 80.00th=[  103], 90.00th=[  110], 95.00th=[  116],
     | 99.00th=[  129], 99.50th=[  137], 99.90th=[  161], 99.95th=[  194],
     | 99.99th=[ 2507]
   bw (  KiB/s): min=21032, max=25360, per=100.00%, avg=22829.60, stdev=1168.54, samples=20
   iops        : min= 5258, max= 6340, avg=5707.40, stdev=292.13, samples=20
  lat (usec)   : 50=0.04%, 100=85.01%, 250=14.92%, 500=0.01%, 750=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%, 10=0.01%, 50=0.01%
  cpu          : usr=9.00%, sys=31.89%, ctx=114467, majf=0, minf=308
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=57310,57074,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=22.4MiB/s (23.5MB/s), 22.4MiB/s-22.4MiB/s (23.5MB/s-23.5MB/s), io=224MiB (235MB), run=10001-10001msec
  WRITE: bw=22.3MiB/s (23.4MB/s), 22.3MiB/s-22.3MiB/s (23.4MB/s-23.4MB/s), io=223MiB (234MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/126, sectors=0/38600, merge=0/994, ticks=0/166, in_queue=171, util=0.14%
```
