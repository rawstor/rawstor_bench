[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2026-11-20 10:30:46

refs/heads/add/list-by-location

[a23f3a5](https://github.com/rawstor/librawstor/commit/a23f3a5bf1aec5777cdd731d4bfbfe89e85fdd79)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16287: Fri Nov 20 10:29:33 2026
  read: IOPS=367k, BW=1433MiB/s (1502MB/s)(14.0GiB/10001msec)
    slat (nsec): min=200, max=165315, avg=313.32, stdev=239.82
    clat (usec): min=2, max=542, avg= 4.95, stdev= 2.08
     lat (usec): min=2, max=542, avg= 5.26, stdev= 2.09
    clat percentiles (nsec):
     |  1.00th=[ 3056],  5.00th=[ 3312], 10.00th=[ 3568], 20.00th=[ 4192],
     | 30.00th=[ 4448], 40.00th=[ 4640], 50.00th=[ 4704], 60.00th=[ 4832],
     | 70.00th=[ 4960], 80.00th=[ 5152], 90.00th=[ 6816], 95.00th=[ 7840],
     | 99.00th=[ 8384], 99.50th=[12352], 99.90th=[17792], 99.95th=[21376],
     | 99.99th=[96768]
   bw (  MiB/s): min= 1321, max= 1456, per=100.00%, avg=1433.53, stdev=28.17, samples=20
   iops        : min=338258, max=372807, avg=366984.25, stdev=7211.30, samples=20
  lat (usec)   : 4=17.37%, 10=82.01%, 20=0.56%, 50=0.05%, 100=0.01%
  lat (usec)   : 250=0.01%, 500=0.01%, 750=0.01%
  cpu          : usr=42.21%, sys=57.76%, ctx=228, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3667801,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16291: Fri Nov 20 10:29:33 2026
  write: IOPS=1608, BW=6434KiB/s (6589kB/s)(62.8MiB/10001msec); 0 zone resets
    slat (nsec): min=390, max=19379, avg=1261.33, stdev=1099.03
    clat (usec): min=174, max=307463, avg=1241.39, stdev=6122.29
     lat (usec): min=175, max=307465, avg=1242.66, stdev=6122.55
    clat percentiles (usec):
     |  1.00th=[   215],  5.00th=[   273], 10.00th=[   383], 20.00th=[   469],
     | 30.00th=[   502], 40.00th=[   529], 50.00th=[   545], 60.00th=[   570],
     | 70.00th=[   611], 80.00th=[   709], 90.00th=[   906], 95.00th=[  1713],
     | 99.00th=[ 17957], 99.50th=[ 31851], 99.90th=[ 81265], 99.95th=[141558],
     | 99.99th=[219153]
   bw (  KiB/s): min=  184, max=13034, per=100.00%, avg=6437.20, stdev=4207.14, samples=20
   iops        : min=   46, max= 3258, avg=1609.20, stdev=1051.68, samples=20
  lat (usec)   : 250=3.08%, 500=26.79%, 750=52.56%, 1000=9.03%
  lat (msec)   : 2=4.05%, 4=1.57%, 10=0.91%, 20=1.36%, 50=0.42%
  lat (msec)   : 100=0.16%, 250=0.07%, 500=0.01%
  cpu          : usr=0.76%, sys=3.44%, ctx=32277, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,16086,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=1433MiB/s (1502MB/s), 1433MiB/s-1433MiB/s (1502MB/s-1502MB/s), io=14.0GiB (15.0GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=6434KiB/s (6589kB/s), 6434KiB/s-6434KiB/s (6589kB/s-6589kB/s), io=62.8MiB (65.9MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=0/46663, sectors=0/1664744, merge=0/69097, ticks=0/140260, in_queue=140261, util=49.45%
```
