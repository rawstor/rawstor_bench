[&lt; back](..)

# perftest-ost-4k-1-1

2026-11-19 18:17:12

refs/heads/add/location-list

[02fcc5d](https://github.com/rawstor/librawstor/commit/02fcc5d5df2e8c4351afa33e21fde6bdeba950a9)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16346: Thu Nov 19 18:16:06 2026
  read: IOPS=21.0k, BW=82.0MiB/s (86.0MB/s)(821MiB/10001msec)
    slat (nsec): min=1372, max=55222, avg=2096.80, stdev=918.91
    clat (usec): min=35, max=1354, avg=44.95, stdev=10.81
     lat (usec): min=37, max=1358, avg=47.05, stdev=11.25
    clat percentiles (usec):
     |  1.00th=[   37],  5.00th=[   38], 10.00th=[   38], 20.00th=[   39],
     | 30.00th=[   39], 40.00th=[   40], 50.00th=[   41], 60.00th=[   45],
     | 70.00th=[   50], 80.00th=[   52], 90.00th=[   55], 95.00th=[   59],
     | 99.00th=[   73], 99.50th=[   78], 99.90th=[  163], 99.95th=[  204],
     | 99.99th=[  293]
   bw (  KiB/s): min=70861, max=93400, per=100.00%, avg=84057.70, stdev=6337.42, samples=20
   iops        : min=17715, max=23350, avg=21014.30, stdev=1584.35, samples=20
  lat (usec)   : 50=72.96%, 100=26.81%, 250=0.21%, 500=0.02%, 750=0.01%
  lat (msec)   : 2=0.01%
  cpu          : usr=18.82%, sys=29.89%, ctx=210059, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=210048,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16350: Thu Nov 19 18:16:06 2026
  write: IOPS=2590, BW=10.1MiB/s (10.6MB/s)(101MiB/10001msec); 0 zone resets
    slat (nsec): min=3585, max=36494, avg=6353.06, stdev=1576.88
    clat (usec): min=249, max=38289, avg=378.31, stdev=615.13
     lat (usec): min=255, max=38295, avg=384.67, stdev=615.16
    clat percentiles (usec):
     |  1.00th=[  269],  5.00th=[  281], 10.00th=[  293], 20.00th=[  310],
     | 30.00th=[  322], 40.00th=[  334], 50.00th=[  343], 60.00th=[  351],
     | 70.00th=[  359], 80.00th=[  371], 90.00th=[  396], 95.00th=[  433],
     | 99.00th=[  938], 99.50th=[ 1614], 99.90th=[ 8586], 99.95th=[13435],
     | 99.99th=[30016]
   bw (  KiB/s): min= 9128, max=11200, per=100.00%, avg=10366.95, stdev=543.94, samples=20
   iops        : min= 2282, max= 2800, avg=2591.70, stdev=135.96, samples=20
  lat (usec)   : 250=0.01%, 500=97.56%, 750=1.22%, 1000=0.27%
  lat (msec)   : 2=0.53%, 4=0.18%, 10=0.16%, 20=0.05%, 50=0.02%
  cpu          : usr=4.49%, sys=4.90%, ctx=25908, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,25908,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=82.0MiB/s (86.0MB/s), 82.0MiB/s-82.0MiB/s (86.0MB/s-86.0MB/s), io=821MiB (860MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=10.1MiB/s (10.6MB/s), 10.1MiB/s-10.1MiB/s (10.6MB/s-10.6MB/s), io=101MiB (106MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=1/66716, sectors=8/1518256, merge=0/100494, ticks=1/21995, in_queue=21996, util=32.47%
```
