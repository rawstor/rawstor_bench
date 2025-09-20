[&lt; back](..)

# perftest--without-liburing-4k-2-1

2025-09-20 21:51:21

refs/heads/add/cppringbuf

[bdea762](https://github.com/rawstor/librawstor/commit/bdea76263b1a2eef34f16468cc41bfb0fccfcece)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11413: Sat Sep 20 21:51:19 2025
  read: IOPS=9725, BW=38.0MiB/s (39.8MB/s)(380MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=107, max=10105, avg=5040.22, stdev=2907.27
     lat (usec): min=28, max=31697, avg=95.69, stdev=311.81
    clat percentiles (msec):
     |  1.00th=[  211],  5.00th=[  567], 10.00th=[  995], 20.00th=[ 2022],
     | 30.00th=[ 3004], 40.00th=[ 4010], 50.00th=[ 5000], 60.00th=[ 6007],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=35976, max=45336, per=100.00%, avg=38906.40, stdev=2259.59, samples=20
   iops        : min= 8994, max=11334, avg=9726.60, stdev=564.90, samples=20
  write: IOPS=9703, BW=37.9MiB/s (39.7MB/s)(379MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=107, max=10105, avg=5046.64, stdev=2914.90
     lat (usec): min=50, max=35851, avg=107.56, stdev=318.62
    clat percentiles (msec):
     |  1.00th=[  205],  5.00th=[  567], 10.00th=[  995], 20.00th=[ 2022],
     | 30.00th=[ 3004], 40.00th=[ 4010], 50.00th=[ 5000], 60.00th=[ 6007],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=36232, max=44616, per=100.00%, avg=38816.40, stdev=2056.42, samples=20
   iops        : min= 9058, max=11154, avg=9704.10, stdev=514.11, samples=20
  lat (msec)   : 250=1.49%, 500=2.74%, 750=2.81%, 1000=3.00%, 2000=9.84%
  lat (msec)   : >=2000=80.12%
  cpu          : usr=10.33%, sys=37.44%, ctx=104467, majf=0, minf=293
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=97266,97041,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=38.0MiB/s (39.8MB/s), 38.0MiB/s-38.0MiB/s (39.8MB/s-39.8MB/s), io=380MiB (398MB), run=10001-10001msec
  WRITE: bw=37.9MiB/s (39.7MB/s), 37.9MiB/s-37.9MiB/s (39.7MB/s-39.7MB/s), io=379MiB (397MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/299, sectors=0/43416, merge=0/1766, ticks=0/954, in_queue=961, util=0.20%
```
