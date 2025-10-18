[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2025-10-18 20:38:15

refs/heads/test/asan

[faa6023](https://github.com/rawstor/librawstor/commit/faa6023e2edfba88ac376fc2a65a2e5ed572cac6)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10746: Sat Oct 18 20:38:13 2025
  read: IOPS=170k, BW=665MiB/s (697MB/s)(6652MiB/10001msec)
    slat (nsec): min=9, max=19366, avg=30.13, stdev=61.22
    clat (nsec): min=1664, max=89438, avg=2337.17, stdev=1174.70
     lat (nsec): min=1693, max=89808, avg=2367.30, stdev=1177.66
    clat percentiles (nsec):
     |  1.00th=[ 1960],  5.00th=[ 2008], 10.00th=[ 2040], 20.00th=[ 2064],
     | 30.00th=[ 2096], 40.00th=[ 2128], 50.00th=[ 2128], 60.00th=[ 2160],
     | 70.00th=[ 2192], 80.00th=[ 2224], 90.00th=[ 2416], 95.00th=[ 3472],
     | 99.00th=[ 6816], 99.50th=[10816], 99.90th=[16512], 99.95th=[19840],
     | 99.99th=[28544]
   bw (  KiB/s): min=376048, max=760040, per=99.50%, avg=677615.00, stdev=119450.85, samples=19
   iops        : min=94012, max=190010, avg=169403.74, stdev=29862.75, samples=19
  write: IOPS=170k, BW=665MiB/s (697MB/s)(6646MiB/10001msec); 0 zone resets
    slat (nsec): min=29, max=17302, avg=43.92, stdev=71.98
    clat (nsec): min=2153, max=80481, avg=2947.43, stdev=1153.27
     lat (nsec): min=2204, max=80531, avg=2991.35, stdev=1157.57
    clat percentiles (nsec):
     |  1.00th=[ 2352],  5.00th=[ 2416], 10.00th=[ 2416], 20.00th=[ 2480],
     | 30.00th=[ 2480], 40.00th=[ 2512], 50.00th=[ 2512], 60.00th=[ 2544],
     | 70.00th=[ 2576], 80.00th=[ 2768], 90.00th=[ 4768], 95.00th=[ 5088],
     | 99.00th=[ 6176], 99.50th=[ 7840], 99.90th=[14144], 99.95th=[15808],
     | 99.99th=[22656]
   bw (  KiB/s): min=376304, max=759520, per=99.49%, avg=677020.26, stdev=119380.09, samples=19
   iops        : min=94076, max=189880, avg=169255.05, stdev=29845.05, samples=19
  lat (usec)   : 2=2.38%, 4=88.61%, 10=8.57%, 20=0.40%, 50=0.03%
  lat (usec)   : 100=0.01%
  cpu          : usr=30.05%, sys=69.93%, ctx=71, majf=0, minf=35
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1702786,1701346,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=665MiB/s (697MB/s), 665MiB/s-665MiB/s (697MB/s-697MB/s), io=6652MiB (6975MB), run=10001-10001msec
  WRITE: bw=665MiB/s (697MB/s), 665MiB/s-665MiB/s (697MB/s-697MB/s), io=6646MiB (6969MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/12, sectors=0/2032, merge=0/28, ticks=0/8, in_queue=8, util=0.01%
```
