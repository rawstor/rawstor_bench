[&lt; back](..)

# perftest--without-liburing-4k-1-1

2025-09-28 20:09:31

refs/heads/add/socket

[5dded36](https://github.com/rawstor/librawstor/commit/5dded36e9d4baaed3055c2d7bddf2e03e51fd1da)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11672: Sun Sep 28 20:09:28 2025
  read: IOPS=6076, BW=23.7MiB/s (24.9MB/s)(237MiB/10001msec)
    slat (nsec): min=30, max=15288, avg=188.03, stdev=189.88
    clat (usec): min=41, max=25614, avg=68.65, stdev=142.62
     lat (usec): min=41, max=25615, avg=68.84, stdev=142.62
    clat percentiles (usec):
     |  1.00th=[   52],  5.00th=[   55], 10.00th=[   57], 20.00th=[   60],
     | 30.00th=[   62], 40.00th=[   65], 50.00th=[   67], 60.00th=[   69],
     | 70.00th=[   72], 80.00th=[   75], 90.00th=[   81], 95.00th=[   87],
     | 99.00th=[  100], 99.50th=[  108], 99.90th=[  128], 99.95th=[  153],
     | 99.99th=[  343]
   bw (  KiB/s): min=22936, max=27544, per=100.00%, avg=24309.20, stdev=1229.77, samples=20
   iops        : min= 5734, max= 6886, avg=6077.30, stdev=307.44, samples=20
  write: IOPS=6058, BW=23.7MiB/s (24.8MB/s)(237MiB/10001msec); 0 zone resets
    slat (nsec): min=70, max=22011, avg=257.40, stdev=201.23
    clat (usec): min=57, max=30301, avg=92.65, stdev=227.85
     lat (usec): min=57, max=30302, avg=92.91, stdev=227.85
    clat percentiles (usec):
     |  1.00th=[   73],  5.00th=[   77], 10.00th=[   79], 20.00th=[   82],
     | 30.00th=[   85], 40.00th=[   87], 50.00th=[   89], 60.00th=[   92],
     | 70.00th=[   94], 80.00th=[   98], 90.00th=[  104], 95.00th=[  110],
     | 99.00th=[  124], 99.50th=[  133], 99.90th=[  163], 99.95th=[  204],
     | 99.99th=[ 3326]
   bw (  KiB/s): min=22000, max=26960, per=100.00%, avg=24238.40, stdev=1290.24, samples=20
   iops        : min= 5500, max= 6740, avg=6059.60, stdev=322.56, samples=20
  lat (usec)   : 50=0.15%, 100=91.85%, 250=7.98%, 500=0.01%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%, 10=0.01%, 20=0.01%, 50=0.01%
  cpu          : usr=8.35%, sys=32.69%, ctx=121428, majf=0, minf=303
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=60773,60596,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=23.7MiB/s (24.9MB/s), 23.7MiB/s-23.7MiB/s (24.9MB/s-24.9MB/s), io=237MiB (249MB), run=10001-10001msec
  WRITE: bw=23.7MiB/s (24.8MB/s), 23.7MiB/s-23.7MiB/s (24.8MB/s-24.8MB/s), io=237MiB (248MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/118, sectors=0/36136, merge=0/1089, ticks=0/332, in_queue=337, util=0.15%
```
