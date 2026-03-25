[&lt; back](..)

# perftest-file-4k-2-1

2026-03-25 08:44:39

refs/heads/fix/breakmshot

[1bee1dd](https://github.com/rawstor/librawstor/commit/1bee1dde6e18056b0eebe14ea59f695d43bfca5d)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=10693: Wed Mar 25 08:43:51 2026
  read: IOPS=450k, BW=1757MiB/s (1842MB/s)(17.2GiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=110, max=10110, avg=5289.07, stdev=2799.91
     lat (usec): min=3, max=174, avg= 4.23, stdev= 1.40
    clat percentiles (msec):
     |  1.00th=[  271],  5.00th=[  944], 10.00th=[ 1435], 20.00th=[ 2400],
     | 30.00th=[ 3373], 40.00th=[ 4329], 50.00th=[ 5269], 60.00th=[ 6275],
     | 70.00th=[ 7215], 80.00th=[ 8221], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  MiB/s): min=  986, max= 1843, per=100.00%, avg=1766.36, stdev=197.21, samples=19
   iops        : min=252440, max=471940, avg=452189.42, stdev=50486.18, samples=19
  lat (msec)   : 250=0.88%, 500=1.40%, 750=1.31%, 1000=1.98%, 2000=10.27%
  lat (msec)   : >=2000=84.17%
  cpu          : usr=32.80%, sys=67.18%, ctx=79, majf=0, minf=23
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=4498358,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=10696: Wed Mar 25 08:43:51 2026
  write: IOPS=66.2k, BW=258MiB/s (271MB/s)(2585MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=10324, max=20323, avg=15549.58, stdev=2862.98
     lat (usec): min=4, max=936, avg=29.74, stdev= 6.30
    clat percentiles (msec):
     |  1.00th=[10402],  5.00th=[10939], 10.00th=[11476], 20.00th=[12550],
     | 30.00th=[13758], 40.00th=[14832], 50.00th=[15637], 60.00th=[16576],
     | 70.00th=[17113], 80.00th=[17113], 90.00th=[17113], 95.00th=[17113],
     | 99.00th=[17113], 99.50th=[17113], 99.90th=[17113], 99.95th=[17113],
     | 99.99th=[17113]
   bw (  KiB/s): min=212936, max=291424, per=99.57%, avg=263560.00, stdev=26905.13, samples=19
   iops        : min=53234, max=72856, avg=65890.00, stdev=6726.31, samples=19
  lat (msec)   : >=2000=100.00%
  cpu          : usr=14.49%, sys=34.82%, ctx=330072, majf=0, minf=22
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,661801,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=1757MiB/s (1842MB/s), 1757MiB/s-1757MiB/s (1842MB/s-1842MB/s), io=17.2GiB (18.4GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=258MiB/s (271MB/s), 258MiB/s-258MiB/s (271MB/s-271MB/s), io=2585MiB (2711MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/354, sectors=0/86560, merge=0/1366, ticks=0/493, in_queue=498, util=0.19%
```
