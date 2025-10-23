[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2025-10-23 21:01:25

refs/heads/ci/packages

[2a80f1a](https://github.com/rawstor/librawstor/commit/2a80f1a23bf5dca2fcbe4d8b4066d8bea57c41bc)

rw = randrw, bs = 4k, iodepth = 2, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=10928: Thu Oct 23 21:01:23 2025
  read: IOPS=168k, BW=656MiB/s (688MB/s)(6559MiB/10001msec)
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10110, avg=5516.79, stdev=2737.48
     lat (nsec): min=1683, max=254836, avg=2365.36, stdev=1754.95
    clat percentiles (msec):
     |  1.00th=[  275],  5.00th=[  995], 10.00th=[ 1687], 20.00th=[ 2769],
     | 30.00th=[ 3742], 40.00th=[ 4732], 50.00th=[ 5604], 60.00th=[ 6477],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9597],
     | 99.00th=[10000], 99.50th=[10134], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=351472, max=755392, per=99.47%, avg=667972.21, stdev=122491.01, samples=19
   iops        : min=87868, max=188848, avg=166993.05, stdev=30622.75, samples=19
  write: IOPS=168k, BW=655MiB/s (687MB/s)(6553MiB/10001msec); 0 zone resets
    slat (nsec): min=0, max=0, avg= 0.00, stdev= 0.00
    clat (msec): min=111, max=10110, avg=5517.99, stdev=2737.92
     lat (usec): min=4, max=321, avg= 9.02, stdev= 5.26
    clat percentiles (msec):
     |  1.00th=[  275],  5.00th=[ 1003], 10.00th=[ 1687], 20.00th=[ 2769],
     | 30.00th=[ 3742], 40.00th=[ 4732], 50.00th=[ 5604], 60.00th=[ 6544],
     | 70.00th=[ 7416], 80.00th=[ 8288], 90.00th=[ 9194], 95.00th=[ 9731],
     | 99.00th=[10000], 99.50th=[10000], 99.90th=[10134], 99.95th=[10134],
     | 99.99th=[10134]
   bw (  KiB/s): min=351224, max=755936, per=99.45%, avg=667298.53, stdev=122383.56, samples=19
   iops        : min=87806, max=188984, avg=166824.63, stdev=30595.89, samples=19
  lat (msec)   : 250=0.86%, 500=1.49%, 750=1.39%, 1000=1.26%, 2000=7.76%
  lat (msec)   : >=2000=87.23%
  cpu          : usr=29.99%, sys=69.99%, ctx=65, majf=0, minf=36
  IO depths    : 1=0.1%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=1679043,1677670,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=656MiB/s (688MB/s), 656MiB/s-656MiB/s (688MB/s-688MB/s), io=6559MiB (6877MB), run=10001-10001msec
  WRITE: bw=655MiB/s (687MB/s), 655MiB/s-655MiB/s (687MB/s-687MB/s), io=6553MiB (6872MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/40, sectors=0/9512, merge=0/171, ticks=0/54, in_queue=53, util=0.01%
```
