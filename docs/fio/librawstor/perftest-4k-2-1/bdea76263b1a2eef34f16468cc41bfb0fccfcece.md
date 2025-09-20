[&lt; back](..)

# perftest-4k-2-1

2025-09-20 21:52:00

refs/heads/add/cppringbuf

[bdea762](https://github.com/rawstor/librawstor/commit/bdea76263b1a2eef34f16468cc41bfb0fccfcece)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11323: Sat Sep 20 21:51:58 2025
  read: IOPS=10.9k, BW=42.7MiB/s (44.7MB/s)(427MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5058.46, stdev=2911.20
     lat (usec): min=27, max=30410, avg=79.48, stdev=291.71
    clat percentiles (msec):
     |  1.00th=[  211],  5.00th=[  575], 10.00th=[ 1020], 20.00th=[ 1989],
     | 30.00th=[ 3004], 40.00th=[ 4044], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=41104, max=49416, per=100.00%, avg=43737.26, stdev=2522.66, samples=19
   iops        : min=10276, max=12354, avg=10934.32, stdev=630.67, samples=19
  write: IOPS=10.9k, BW=42.5MiB/s (44.6MB/s)(425MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=106, max=10105, avg=5060.02, stdev=2913.13
     lat (usec): min=41, max=31651, avg=101.30, stdev=270.30
    clat percentiles (msec):
     |  1.00th=[  205],  5.00th=[  575], 10.00th=[ 1020], 20.00th=[ 1989],
     | 30.00th=[ 3004], 40.00th=[ 4077], 50.00th=[ 5067], 60.00th=[ 6074],
     | 70.00th=[ 7080], 80.00th=[ 8087], 90.00th=[ 9060], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=40344, max=48696, per=100.00%, avg=43659.37, stdev=2204.71, samples=19
   iops        : min=10086, max=12174, avg=10914.84, stdev=551.18, samples=19
  lat (msec)   : 250=1.46%, 500=2.72%, 750=2.84%, 1000=2.80%, 2000=10.30%
  lat (msec)   : >=2000=79.88%
  cpu          : usr=8.67%, sys=50.93%, ctx=145359, majf=0, minf=289
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=109244,108925,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=42.7MiB/s (44.7MB/s), 42.7MiB/s-42.7MiB/s (44.7MB/s-44.7MB/s), io=427MiB (447MB), run=10001-10001msec
  WRITE: bw=42.5MiB/s (44.6MB/s), 42.5MiB/s-42.5MiB/s (44.6MB/s-44.6MB/s), io=425MiB (446MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/113, sectors=0/39000, merge=0/1073, ticks=0/209, in_queue=219, util=0.20%
```
