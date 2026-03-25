[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2026-03-25 08:44:39

refs/heads/fix/breakmshot

[1bee1dd](https://github.com/rawstor/librawstor/commit/1bee1dde6e18056b0eebe14ea59f695d43bfca5d)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=10798: Wed Mar 25 08:44:05 2026
  read: IOPS=334k, BW=1304MiB/s (1368MB/s)(12.7GiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=109, max=10109, avg=5261.47, stdev=2812.84
     lat (usec): min=4, max=102, avg= 5.73, stdev= 1.53
    clat percentiles (msec):
     |  1.00th=[  255],  5.00th=[  885], 10.00th=[ 1401], 20.00th=[ 2366],
     | 30.00th=[ 3339], 40.00th=[ 4329], 50.00th=[ 5269], 60.00th=[ 6275],
     | 70.00th=[ 7215], 80.00th=[ 8154], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  MiB/s): min=  839, max= 1369, per=100.00%, avg=1309.81, stdev=126.41, samples=19
   iops        : min=214987, max=350548, avg=335310.26, stdev=32361.32, samples=19
  lat (msec)   : 250=0.97%, 500=1.64%, 750=1.51%, 1000=1.83%, 2000=10.29%
  lat (msec)   : >=2000=83.76%
  cpu          : usr=45.58%, sys=54.40%, ctx=64, majf=0, minf=39
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3339634,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=10800: Wed Mar 25 08:44:05 2026
  write: IOPS=272k, BW=1064MiB/s (1116MB/s)(10.4GiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=10320, max=20320, avg=15553.50, stdev=2785.60
     lat (usec): min=5, max=108, avg= 7.07, stdev= 1.59
    clat percentiles (msec):
     |  1.00th=[10537],  5.00th=[11073], 10.00th=[11745], 20.00th=[12684],
     | 30.00th=[13624], 40.00th=[14563], 50.00th=[15637], 60.00th=[16576],
     | 70.00th=[17113], 80.00th=[17113], 90.00th=[17113], 95.00th=[17113],
     | 99.00th=[17113], 99.50th=[17113], 99.90th=[17113], 99.95th=[17113],
     | 99.99th=[17113]
   bw (  MiB/s): min=  705, max= 1132, per=99.72%, avg=1061.09, stdev=141.69, samples=19
   iops        : min=180502, max=289968, avg=271638.11, stdev=36271.79, samples=19
  lat (msec)   : >=2000=100.00%
  cpu          : usr=39.29%, sys=60.69%, ctx=65, majf=0, minf=37
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,2724246,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=1304MiB/s (1368MB/s), 1304MiB/s-1304MiB/s (1368MB/s-1368MB/s), io=12.7GiB (13.7GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=1064MiB/s (1116MB/s), 1064MiB/s-1064MiB/s (1116MB/s-1116MB/s), io=10.4GiB (11.2GB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/373, sectors=0/89448, merge=0/1249, ticks=0/576, in_queue=579, util=0.14%
```
