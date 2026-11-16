[&lt; back](..)

# perftest-ost-4k-2-1

2026-11-16 21:04:41

refs/heads/add/security-authorization

[bad7dc5](https://github.com/rawstor/librawstor/commit/bad7dc5e9daf991dedda6e426d6eb5ed774ca05d)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16222: Mon Nov 16 21:03:58 2026
  read: IOPS=42.4k, BW=166MiB/s (174MB/s)(1658MiB/10001msec)
    slat (nsec): min=350, max=979703, avg=1747.49, stdev=4714.88
    clat (usec): min=22, max=3362, avg=44.96, stdev=55.53
     lat (usec): min=23, max=3364, avg=46.71, stdev=56.80
    clat percentiles (usec):
     |  1.00th=[   24],  5.00th=[   25], 10.00th=[   26], 20.00th=[   32],
     | 30.00th=[   34], 40.00th=[   35], 50.00th=[   36], 60.00th=[   38],
     | 70.00th=[   40], 80.00th=[   44], 90.00th=[   56], 95.00th=[   84],
     | 99.00th=[  247], 99.50th=[  371], 99.90th=[  734], 99.95th=[ 1004],
     | 99.99th=[ 1663]
   bw (  KiB/s): min=63519, max=224008, per=100.00%, avg=169898.80, stdev=52642.15, samples=20
   iops        : min=15879, max=56002, avg=42474.55, stdev=13160.63, samples=20
  lat (usec)   : 50=86.37%, 100=9.78%, 250=2.87%, 500=0.71%, 750=0.18%
  lat (usec)   : 1000=0.04%
  lat (msec)   : 2=0.05%, 4=0.01%
  cpu          : usr=30.96%, sys=46.31%, ctx=177577, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=424450,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16227: Mon Nov 16 21:03:58 2026
  write: IOPS=3628, BW=14.2MiB/s (14.9MB/s)(142MiB/10002msec); 0 zone resets
    slat (nsec): min=681, max=860327, avg=6576.69, stdev=5055.78
    clat (usec): min=257, max=89058, avg=543.45, stdev=2068.01
     lat (usec): min=263, max=89065, avg=550.03, stdev=2068.11
    clat percentiles (usec):
     |  1.00th=[  285],  5.00th=[  302], 10.00th=[  318], 20.00th=[  338],
     | 30.00th=[  359], 40.00th=[  375], 50.00th=[  388], 60.00th=[  408],
     | 70.00th=[  437], 80.00th=[  498], 90.00th=[  603], 95.00th=[  750],
     | 99.00th=[ 1975], 99.50th=[ 4883], 99.90th=[27395], 99.95th=[55313],
     | 99.99th=[87557]
   bw (  KiB/s): min= 7752, max=18861, per=100.00%, avg=14522.95, stdev=3478.77, samples=20
   iops        : min= 1938, max= 4715, avg=3630.65, stdev=869.66, samples=20
  lat (usec)   : 500=80.45%, 750=14.56%, 1000=2.14%
  lat (msec)   : 2=1.87%, 4=0.39%, 10=0.34%, 20=0.13%, 50=0.06%
  lat (msec)   : 100=0.06%
  cpu          : usr=6.00%, sys=8.03%, ctx=33842, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,36289,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=166MiB/s (174MB/s), 166MiB/s-166MiB/s (174MB/s-174MB/s), io=1658MiB (1739MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=14.2MiB/s (14.9MB/s), 14.2MiB/s-14.2MiB/s (14.9MB/s-14.9MB/s), io=142MiB (149MB), run=10002-10002msec

Disk stats (read/write):
  nvme0n1: ios=2/84147, sectors=16/1858584, merge=0/125213, ticks=2/21840, in_queue=21842, util=38.24%
```
