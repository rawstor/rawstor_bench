[&lt; back](..)

# perftest-ost-4k-1-1

2025-10-18 20:39:15

refs/heads/test/asan

[faa6023](https://github.com/rawstor/librawstor/commit/faa6023e2edfba88ac376fc2a65a2e5ed572cac6)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11649: Sat Oct 18 20:39:13 2025
  read: IOPS=5734, BW=22.4MiB/s (23.5MB/s)(224MiB/10001msec)
    slat (nsec): min=40, max=22171, avg=162.52, stdev=224.10
    clat (usec): min=38, max=25153, avg=72.39, stdev=168.80
     lat (usec): min=38, max=25153, avg=72.55, stdev=168.80
    clat percentiles (usec):
     |  1.00th=[   53],  5.00th=[   58], 10.00th=[   60], 20.00th=[   63],
     | 30.00th=[   66], 40.00th=[   69], 50.00th=[   71], 60.00th=[   73],
     | 70.00th=[   75], 80.00th=[   78], 90.00th=[   84], 95.00th=[   90],
     | 99.00th=[  105], 99.50th=[  113], 99.90th=[  145], 99.95th=[  176],
     | 99.99th=[ 1057]
   bw (  KiB/s): min=20776, max=24624, per=100.00%, avg=22941.20, stdev=971.20, samples=20
   iops        : min= 5194, max= 6156, avg=5735.30, stdev=242.80, samples=20
  write: IOPS=5711, BW=22.3MiB/s (23.4MB/s)(223MiB/10001msec); 0 zone resets
    slat (nsec): min=80, max=18183, avg=245.46, stdev=240.87
    clat (usec): min=55, max=26314, avg=98.57, stdev=198.62
     lat (usec): min=56, max=26314, avg=98.82, stdev=198.62
    clat percentiles (usec):
     |  1.00th=[   76],  5.00th=[   81], 10.00th=[   85], 20.00th=[   88],
     | 30.00th=[   91], 40.00th=[   93], 50.00th=[   96], 60.00th=[   98],
     | 70.00th=[  101], 80.00th=[  104], 90.00th=[  111], 95.00th=[  117],
     | 99.00th=[  133], 99.50th=[  143], 99.90th=[  200], 99.95th=[  269],
     | 99.99th=[ 1319]
   bw (  KiB/s): min=21504, max=24968, per=100.00%, avg=22849.60, stdev=951.78, samples=20
   iops        : min= 5376, max= 6242, avg=5712.40, stdev=237.95, samples=20
  lat (usec)   : 50=0.20%, 100=82.82%, 250=16.94%, 500=0.02%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%, 20=0.01%, 50=0.01%
  cpu          : usr=7.59%, sys=34.24%, ctx=115118, majf=0, minf=43
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=57353,57124,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=22.4MiB/s (23.5MB/s), 22.4MiB/s-22.4MiB/s (23.5MB/s-23.5MB/s), io=224MiB (235MB), run=10001-10001msec
  WRITE: bw=22.3MiB/s (23.4MB/s), 22.3MiB/s-22.3MiB/s (23.4MB/s-23.4MB/s), io=223MiB (234MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/133, sectors=0/38560, merge=0/1017, ticks=0/137, in_queue=144, util=0.21%
```
