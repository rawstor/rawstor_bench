[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2025-10-06 09:56:52

refs/heads/add/uri

[7d5ccdc](https://github.com/rawstor/librawstor/commit/7d5ccdce3ba82ca4a4ebd0dd1adf6e8799c84a40)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10801: Mon Oct  6 09:56:49 2025
  read: IOPS=177k, BW=690MiB/s (723MB/s)(6898MiB/10001msec)
    slat (nsec): min=9, max=21240, avg=25.46, stdev=52.61
    clat (nsec): min=1593, max=112900, avg=2216.76, stdev=1189.10
     lat (nsec): min=1623, max=112960, avg=2242.22, stdev=1191.39
    clat percentiles (nsec):
     |  1.00th=[ 1816],  5.00th=[ 1896], 10.00th=[ 1912], 20.00th=[ 1944],
     | 30.00th=[ 1976], 40.00th=[ 1992], 50.00th=[ 2008], 60.00th=[ 2040],
     | 70.00th=[ 2064], 80.00th=[ 2128], 90.00th=[ 2288], 95.00th=[ 3376],
     | 99.00th=[ 6624], 99.50th=[10432], 99.90th=[16512], 99.95th=[19840],
     | 99.99th=[28544]
   bw (  KiB/s): min=381096, max=779864, per=99.56%, avg=703213.47, stdev=123845.10, samples=19
   iops        : min=95274, max=194966, avg=175803.47, stdev=30961.33, samples=19
  write: IOPS=176k, BW=689MiB/s (723MB/s)(6891MiB/10001msec); 0 zone resets
    slat (nsec): min=29, max=16000, avg=40.37, stdev=63.13
    clat (nsec): min=2063, max=99926, avg=2856.08, stdev=1099.40
     lat (nsec): min=2103, max=99966, avg=2896.44, stdev=1103.00
    clat percentiles (nsec):
     |  1.00th=[ 2288],  5.00th=[ 2352], 10.00th=[ 2384], 20.00th=[ 2384],
     | 30.00th=[ 2416], 40.00th=[ 2448], 50.00th=[ 2480], 60.00th=[ 2480],
     | 70.00th=[ 2544], 80.00th=[ 2704], 90.00th=[ 4512], 95.00th=[ 4896],
     | 99.00th=[ 5856], 99.50th=[ 7520], 99.90th=[13760], 99.95th=[15296],
     | 99.99th=[21632]
   bw (  KiB/s): min=381368, max=776864, per=99.58%, avg=702632.42, stdev=123742.02, samples=19
   iops        : min=95342, max=194216, avg=175658.11, stdev=30935.50, samples=19
  lat (usec)   : 2=20.71%, 4=70.74%, 10=8.13%, 20=0.38%, 50=0.03%
  lat (usec)   : 100=0.01%, 250=0.01%
  cpu          : usr=30.07%, sys=69.92%, ctx=61, majf=0, minf=40
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1765968,1764157,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=690MiB/s (723MB/s), 690MiB/s-690MiB/s (723MB/s-723MB/s), io=6898MiB (7233MB), run=10001-10001msec
  WRITE: bw=689MiB/s (723MB/s), 689MiB/s-689MiB/s (723MB/s-723MB/s), io=6891MiB (7226MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/21, sectors=0/9528, merge=0/44, ticks=0/18, in_queue=18, util=0.02%
```
