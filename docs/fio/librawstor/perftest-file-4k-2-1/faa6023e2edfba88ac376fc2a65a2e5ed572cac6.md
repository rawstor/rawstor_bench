[&lt; back](..)

# perftest-file-4k-2-1

2025-10-18 20:38:13

refs/heads/test/asan

[faa6023](https://github.com/rawstor/librawstor/commit/faa6023e2edfba88ac376fc2a65a2e5ed572cac6)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10736: Sat Oct 18 20:38:11 2025
  read: IOPS=64.4k, BW=252MiB/s (264MB/s)(2516MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10111, avg=5380.80, stdev=2808.60
     lat (nsec): min=1433, max=95219, avg=5331.31, stdev=3766.12
    clat percentiles (msec):
     |  1.00th=[  243],  5.00th=[  776], 10.00th=[ 1435], 20.00th=[ 2534],
     | 30.00th=[ 3507], 40.00th=[ 4530], 50.00th=[ 5470], 60.00th=[ 6409],
     | 70.00th=[ 7349], 80.00th=[ 8221], 90.00th=[ 9194], 95.00th=[ 9731],
     | 99.00th=[10000], 99.50th=[10134], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=192784, max=294544, per=99.31%, avg=255798.74, stdev=30797.84, samples=19
   iops        : min=48196, max=73636, avg=63949.68, stdev=7699.46, samples=19
  write: IOPS=64.4k, BW=251MiB/s (264MB/s)(2514MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10111, avg=5382.82, stdev=2810.02
     lat (usec): min=3, max=1143, avg=24.79, stdev= 7.71
    clat percentiles (msec):
     |  1.00th=[  243],  5.00th=[  776], 10.00th=[ 1452], 20.00th=[ 2534],
     | 30.00th=[ 3540], 40.00th=[ 4530], 50.00th=[ 5470], 60.00th=[ 6409],
     | 70.00th=[ 7349], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9731],
     | 99.00th=[10000], 99.50th=[10134], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=191000, max=293784, per=99.25%, avg=255485.05, stdev=30760.08, samples=19
   iops        : min=47750, max=73446, avg=63871.26, stdev=7690.02, samples=19
  lat (msec)   : 250=1.06%, 500=1.86%, 750=1.89%, 1000=1.85%, 2000=8.24%
  lat (msec)   : >=2000=85.10%
  cpu          : usr=17.97%, sys=49.01%, ctx=273510, majf=0, minf=23
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=643973,643580,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=252MiB/s (264MB/s), 252MiB/s-252MiB/s (264MB/s-264MB/s), io=2516MiB (2638MB), run=10001-10001msec
  WRITE: bw=251MiB/s (264MB/s), 251MiB/s-251MiB/s (264MB/s-264MB/s), io=2514MiB (2636MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/12, sectors=0/2056, merge=0/29, ticks=0/6, in_queue=7, util=0.00%
```
