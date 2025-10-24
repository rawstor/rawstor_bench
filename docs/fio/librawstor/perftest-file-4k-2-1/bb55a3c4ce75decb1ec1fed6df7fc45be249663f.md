[&lt; back](..)

# perftest-file-4k-2-1

2025-10-24 06:47:58

refs/heads/ci/packages

[bb55a3c](https://github.com/rawstor/librawstor/commit/bb55a3c4ce75decb1ec1fed6df7fc45be249663f)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10914: Fri Oct 24 06:47:56 2025
  read: IOPS=68.3k, BW=267MiB/s (280MB/s)(2668MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=113, max=10112, avg=5344.58, stdev=2827.44
     lat (nsec): min=1413, max=116116, avg=5400.96, stdev=3715.51
    clat percentiles (msec):
     |  1.00th=[  239],  5.00th=[  751], 10.00th=[ 1368], 20.00th=[ 2433],
     | 30.00th=[ 3507], 40.00th=[ 4530], 50.00th=[ 5403], 60.00th=[ 6342],
     | 70.00th=[ 7282], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=213216, max=321064, per=99.83%, avg=272732.63, stdev=29414.09, samples=19
   iops        : min=53304, max=80266, avg=68183.16, stdev=7353.52, samples=19
  write: IOPS=68.2k, BW=266MiB/s (279MB/s)(2665MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=113, max=10112, avg=5343.63, stdev=2827.26
     lat (usec): min=3, max=1244, avg=22.89, stdev= 7.28
    clat percentiles (msec):
     |  1.00th=[  236],  5.00th=[  751], 10.00th=[ 1368], 20.00th=[ 2433],
     | 30.00th=[ 3507], 40.00th=[ 4463], 50.00th=[ 5403], 60.00th=[ 6342],
     | 70.00th=[ 7282], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=212880, max=323096, per=99.88%, avg=272543.58, stdev=29365.21, samples=19
   iops        : min=53220, max=80774, avg=68135.89, stdev=7341.30, samples=19
  lat (msec)   : 250=1.10%, 500=1.87%, 750=2.02%, 1000=2.18%, 2000=8.55%
  lat (msec)   : >=2000=84.27%
  cpu          : usr=19.39%, sys=49.43%, ctx=279150, majf=0, minf=21
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=683089,682250,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=267MiB/s (280MB/s), 267MiB/s-267MiB/s (280MB/s-280MB/s), io=2668MiB (2798MB), run=10001-10001msec
  WRITE: bw=266MiB/s (279MB/s), 266MiB/s-266MiB/s (279MB/s-279MB/s), io=2665MiB (2794MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=33/8, sectors=6704/5024, merge=0/36, ticks=174/12, in_queue=187, util=1.05%
```
