[&lt; back](..)

# perftest--disable-ost-4k-2-1

2025-09-28 19:24:25

refs/heads/add/socket

[59db35b](https://github.com/rawstor/librawstor/commit/59db35bd6ebcdf6b432b4e94a18dfaaa3c59c0ca)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10603: Sun Sep 28 19:24:22 2025
  read: IOPS=69.0k, BW=269MiB/s (283MB/s)(2695MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10110, avg=5393.23, stdev=2802.91
     lat (nsec): min=1332, max=154569, avg=5160.68, stdev=3825.94
    clat percentiles (msec):
     |  1.00th=[  232],  5.00th=[  743], 10.00th=[ 1351], 20.00th=[ 2601],
     | 30.00th=[ 3608], 40.00th=[ 4597], 50.00th=[ 5470], 60.00th=[ 6409],
     | 70.00th=[ 7349], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=216240, max=321824, per=99.80%, avg=275411.79, stdev=35246.54, samples=19
   iops        : min=54060, max=80456, avg=68852.95, stdev=8811.64, samples=19
  write: IOPS=68.9k, BW=269MiB/s (282MB/s)(2692MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10110, avg=5392.20, stdev=2802.58
     lat (usec): min=3, max=864, avg=22.90, stdev= 7.10
    clat percentiles (msec):
     |  1.00th=[  232],  5.00th=[  743], 10.00th=[ 1368], 20.00th=[ 2601],
     | 30.00th=[ 3608], 40.00th=[ 4597], 50.00th=[ 5470], 60.00th=[ 6409],
     | 70.00th=[ 7349], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=214536, max=317656, per=99.84%, avg=275173.89, stdev=34924.42, samples=19
   iops        : min=53634, max=79414, avg=68793.47, stdev=8731.05, samples=19
  lat (msec)   : 250=1.14%, 500=1.94%, 750=1.97%, 1000=1.92%, 2000=8.00%
  lat (msec)   : >=2000=85.04%
  cpu          : usr=17.52%, sys=49.79%, ctx=284454, majf=0, minf=28
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=689955,689083,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=269MiB/s (283MB/s), 269MiB/s-269MiB/s (283MB/s-283MB/s), io=2695MiB (2826MB), run=10001-10001msec
  WRITE: bw=269MiB/s (282MB/s), 269MiB/s-269MiB/s (282MB/s-282MB/s), io=2692MiB (2822MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/26, sectors=0/9160, merge=0/150, ticks=0/39, in_queue=39, util=0.01%
```
