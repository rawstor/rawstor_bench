[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2025-10-18 20:38:28

refs/heads/test/asan

[faa6023](https://github.com/rawstor/librawstor/commit/faa6023e2edfba88ac376fc2a65a2e5ed572cac6)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10752: Sat Oct 18 20:38:25 2025
  read: IOPS=169k, BW=660MiB/s (692MB/s)(6604MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5494.43, stdev=2731.91
     lat (nsec): min=1733, max=104966, avg=2380.12, stdev=1195.33
    clat percentiles (msec):
     |  1.00th=[  284],  5.00th=[  995], 10.00th=[ 1687], 20.00th=[ 2769],
     | 30.00th=[ 3742], 40.00th=[ 4665], 50.00th=[ 5604], 60.00th=[ 6477],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=373352, max=756512, per=99.54%, avg=673114.53, stdev=121995.11, samples=19
   iops        : min=93338, max=189128, avg=168278.63, stdev=30498.78, samples=19
  write: IOPS=169k, BW=660MiB/s (692MB/s)(6599MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=105, max=10104, avg=5495.76, stdev=2732.42
     lat (usec): min=4, max=171, avg= 8.94, stdev= 4.69
    clat percentiles (msec):
     |  1.00th=[  284],  5.00th=[  995], 10.00th=[ 1687], 20.00th=[ 2769],
     | 30.00th=[ 3742], 40.00th=[ 4665], 50.00th=[ 5604], 60.00th=[ 6477],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=374016, max=752504, per=99.54%, avg=672563.79, stdev=121912.86, samples=19
   iops        : min=93504, max=188126, avg=168140.95, stdev=30478.21, samples=19
  lat (msec)   : 250=0.81%, 500=1.46%, 750=1.38%, 1000=1.37%, 2000=7.79%
  lat (msec)   : >=2000=87.19%
  cpu          : usr=29.24%, sys=70.71%, ctx=318, majf=0, minf=36
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1690741,1689407,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=660MiB/s (692MB/s), 660MiB/s-660MiB/s (692MB/s-692MB/s), io=6604MiB (6925MB), run=10001-10001msec
  WRITE: bw=660MiB/s (692MB/s), 660MiB/s-660MiB/s (692MB/s-692MB/s), io=6599MiB (6920MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/17, sectors=0/7336, merge=0/46, ticks=0/20, in_queue=20, util=0.03%
```
