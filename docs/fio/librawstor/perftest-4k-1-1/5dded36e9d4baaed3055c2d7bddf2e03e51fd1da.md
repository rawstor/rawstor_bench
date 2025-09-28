[&lt; back](..)

# perftest-4k-1-1

2025-09-28 20:09:46

refs/heads/add/socket

[5dded36](https://github.com/rawstor/librawstor/commit/5dded36e9d4baaed3055c2d7bddf2e03e51fd1da)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11582: Sun Sep 28 20:09:43 2025
  read: IOPS=6088, BW=23.8MiB/s (24.9MB/s)(238MiB/10001msec)
    slat (nsec): min=40, max=17362, avg=171.39, stdev=221.98
    clat (usec): min=41, max=26274, avg=68.37, stdev=173.59
     lat (usec): min=41, max=26274, avg=68.54, stdev=173.59
    clat percentiles (usec):
     |  1.00th=[   51],  5.00th=[   55], 10.00th=[   57], 20.00th=[   60],
     | 30.00th=[   62], 40.00th=[   64], 50.00th=[   66], 60.00th=[   69],
     | 70.00th=[   71], 80.00th=[   75], 90.00th=[   80], 95.00th=[   86],
     | 99.00th=[  100], 99.50th=[  108], 99.90th=[  133], 99.95th=[  167],
     | 99.99th=[  668]
   bw (  KiB/s): min=22832, max=27464, per=100.00%, avg=24462.74, stdev=1114.33, samples=19
   iops        : min= 5708, max= 6866, avg=6115.68, stdev=278.58, samples=19
  write: IOPS=6072, BW=23.7MiB/s (24.9MB/s)(237MiB/10001msec); 0 zone resets
    slat (nsec): min=70, max=17453, avg=229.71, stdev=207.70
    clat (usec): min=53, max=27511, avg=92.67, stdev=236.82
     lat (usec): min=53, max=27512, avg=92.90, stdev=236.84
    clat percentiles (usec):
     |  1.00th=[   72],  5.00th=[   77], 10.00th=[   80], 20.00th=[   83],
     | 30.00th=[   85], 40.00th=[   87], 50.00th=[   89], 60.00th=[   92],
     | 70.00th=[   94], 80.00th=[   97], 90.00th=[  103], 95.00th=[  110],
     | 99.00th=[  124], 99.50th=[  133], 99.90th=[  169], 99.95th=[  227],
     | 99.99th=[ 2212]
   bw (  KiB/s): min=22504, max=26600, per=100.00%, avg=24369.68, stdev=1039.06, samples=19
   iops        : min= 5626, max= 6650, avg=6092.42, stdev=259.77, samples=19
  lat (usec)   : 50=0.34%, 100=91.91%, 250=7.72%, 500=0.02%, 750=0.01%
  lat (usec)   : 1000=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%, 10=0.01%, 50=0.01%
  cpu          : usr=6.65%, sys=33.69%, ctx=121714, majf=0, minf=298
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=60893,60735,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=23.8MiB/s (24.9MB/s), 23.8MiB/s-23.8MiB/s (24.9MB/s-24.9MB/s), io=238MiB (249MB), run=10001-10001msec
  WRITE: bw=23.7MiB/s (24.9MB/s), 23.7MiB/s-23.7MiB/s (24.9MB/s-24.9MB/s), io=237MiB (249MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/157, sectors=0/36312, merge=0/1027, ticks=0/234, in_queue=239, util=0.19%
```
