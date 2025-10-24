[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2025-10-24 06:47:46

refs/heads/ci/packages

[bb55a3c](https://github.com/rawstor/librawstor/commit/bb55a3c4ce75decb1ec1fed6df7fc45be249663f)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10997: Fri Oct 24 06:47:44 2025
  read: IOPS=172k, BW=672MiB/s (705MB/s)(6721MiB/10001msec)
    slat (nsec): min=9, max=26109, avg=29.90, stdev=60.77
    clat (nsec): min=1653, max=115106, avg=2294.62, stdev=1221.26
     lat (nsec): min=1683, max=115136, avg=2324.52, stdev=1224.36
    clat percentiles (nsec):
     |  1.00th=[ 1928],  5.00th=[ 1960], 10.00th=[ 1992], 20.00th=[ 2008],
     | 30.00th=[ 2040], 40.00th=[ 2064], 50.00th=[ 2096], 60.00th=[ 2128],
     | 70.00th=[ 2128], 80.00th=[ 2192], 90.00th=[ 2352], 95.00th=[ 3408],
     | 99.00th=[ 6816], 99.50th=[10688], 99.90th=[16768], 99.95th=[20096],
     | 99.99th=[28800]
   bw (  KiB/s): min=380320, max=763432, per=100.00%, avg=688233.60, stdev=119672.47, samples=20
   iops        : min=95080, max=190858, avg=172058.40, stdev=29918.12, samples=20
  write: IOPS=172k, BW=671MiB/s (704MB/s)(6715MiB/10001msec); 0 zone resets
    slat (nsec): min=29, max=26550, avg=42.49, stdev=68.68
    clat (usec): min=2, max=131, avg= 2.94, stdev= 1.16
     lat (usec): min=2, max=131, avg= 2.98, stdev= 1.17
    clat percentiles (nsec):
     |  1.00th=[ 2384],  5.00th=[ 2416], 10.00th=[ 2416], 20.00th=[ 2448],
     | 30.00th=[ 2480], 40.00th=[ 2512], 50.00th=[ 2544], 60.00th=[ 2544],
     | 70.00th=[ 2608], 80.00th=[ 2768], 90.00th=[ 4640], 95.00th=[ 4960],
     | 99.00th=[ 6304], 99.50th=[ 7968], 99.90th=[14272], 99.95th=[15808],
     | 99.99th=[23936]
   bw (  KiB/s): min=381600, max=763896, per=100.00%, avg=687576.80, stdev=119533.73, samples=20
   iops        : min=95400, max=190974, avg=171894.20, stdev=29883.43, samples=20
  lat (usec)   : 2=6.84%, 4=84.21%, 10=8.50%, 20=0.41%, 50=0.03%
  lat (usec)   : 100=0.01%, 250=0.01%
  cpu          : usr=28.58%, sys=71.40%, ctx=76, majf=0, minf=37
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1720584,1718942,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=672MiB/s (705MB/s), 672MiB/s-672MiB/s (705MB/s-705MB/s), io=6721MiB (7048MB), run=10001-10001msec
  WRITE: bw=671MiB/s (704MB/s), 671MiB/s-671MiB/s (704MB/s-704MB/s), io=6715MiB (7041MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/84, sectors=0/137552, merge=0/29, ticks=0/186, in_queue=185, util=0.16%
```
