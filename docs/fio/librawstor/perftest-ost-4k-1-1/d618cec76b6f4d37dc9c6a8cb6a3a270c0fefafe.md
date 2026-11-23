[&lt; back](..)

# perftest-ost-4k-1-1

2026-11-23 13:30:22

refs/heads/fix/drop-server-error-log-v0.3

[d618cec](https://github.com/rawstor/librawstor/commit/d618cec76b6f4d37dc9c6a8cb6a3a270c0fefafe)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16403: Mon Nov 23 13:24:30 2026
  read: IOPS=28.5k, BW=111MiB/s (117MB/s)(1114MiB/10001msec)
    slat (nsec): min=972, max=149526, avg=1124.74, stdev=665.25
    clat (usec): min=27, max=648, avg=33.77, stdev= 7.96
     lat (usec): min=28, max=649, avg=34.90, stdev= 8.04
    clat percentiles (usec):
     |  1.00th=[   31],  5.00th=[   31], 10.00th=[   31], 20.00th=[   32],
     | 30.00th=[   32], 40.00th=[   32], 50.00th=[   33], 60.00th=[   34],
     | 70.00th=[   35], 80.00th=[   36], 90.00th=[   38], 95.00th=[   41],
     | 99.00th=[   50], 99.50th=[   57], 99.90th=[  155], 99.95th=[  186],
     | 99.99th=[  306]
   bw (  KiB/s): min=96456, max=120352, per=100.00%, avg=114070.65, stdev=5751.99, samples=20
   iops        : min=24114, max=30088, avg=28517.65, stdev=1437.88, samples=20
  lat (usec)   : 50=99.07%, 100=0.71%, 250=0.20%, 500=0.02%, 750=0.01%
  cpu          : usr=12.80%, sys=34.59%, ctx=285059, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=285058,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16406: Mon Nov 23 13:24:30 2026
  write: IOPS=2824, BW=11.0MiB/s (11.6MB/s)(110MiB/10001msec); 0 zone resets
    slat (nsec): min=1542, max=97287, avg=2285.19, stdev=1584.88
    clat (usec): min=249, max=35916, avg=351.45, stdev=236.78
     lat (usec): min=251, max=35918, avg=353.73, stdev=236.90
    clat percentiles (usec):
     |  1.00th=[  269],  5.00th=[  281], 10.00th=[  293], 20.00th=[  310],
     | 30.00th=[  322], 40.00th=[  330], 50.00th=[  343], 60.00th=[  351],
     | 70.00th=[  359], 80.00th=[  371], 90.00th=[  396], 95.00th=[  420],
     | 99.00th=[  603], 99.50th=[  857], 99.90th=[ 1745], 99.95th=[ 2057],
     | 99.99th=[ 4293]
   bw (  KiB/s): min=10216, max=12096, per=100.00%, avg=11301.30, stdev=554.15, samples=20
   iops        : min= 2554, max= 3024, avg=2825.20, stdev=138.49, samples=20
  lat (usec)   : 250=0.01%, 500=98.21%, 750=1.19%, 1000=0.16%
  lat (msec)   : 2=0.37%, 4=0.05%, 10=0.01%, 50=0.01%
  cpu          : usr=1.62%, sys=3.96%, ctx=28244, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,28244,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=111MiB/s (117MB/s), 111MiB/s-111MiB/s (117MB/s-117MB/s), io=1114MiB (1168MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=11.0MiB/s (11.6MB/s), 11.0MiB/s-11.0MiB/s (11.6MB/s-11.6MB/s), io=110MiB (116MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=2/72519, sectors=16/1638168, merge=0/109236, ticks=30/19485, in_queue=19516, util=36.67%
```
