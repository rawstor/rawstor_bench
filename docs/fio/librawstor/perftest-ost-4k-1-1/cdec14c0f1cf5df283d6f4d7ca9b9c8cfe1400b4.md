[&lt; back](..)

# perftest-ost-4k-1-1

2025-10-24 07:15:29

refs/heads/ci/packages

[cdec14c](https://github.com/rawstor/librawstor/commit/cdec14c0f1cf5df283d6f4d7ca9b9c8cfe1400b4)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11902: Fri Oct 24 07:15:26 2025
  read: IOPS=5995, BW=23.4MiB/s (24.6MB/s)(234MiB/10001msec)
    slat (nsec): min=60, max=16892, avg=166.39, stdev=172.99
    clat (usec): min=40, max=28537, avg=69.50, stdev=178.02
     lat (usec): min=40, max=28537, avg=69.66, stdev=178.02
    clat percentiles (usec):
     |  1.00th=[   52],  5.00th=[   56], 10.00th=[   58], 20.00th=[   61],
     | 30.00th=[   63], 40.00th=[   65], 50.00th=[   68], 60.00th=[   70],
     | 70.00th=[   72], 80.00th=[   75], 90.00th=[   81], 95.00th=[   87],
     | 99.00th=[  100], 99.50th=[  106], 99.90th=[  128], 99.95th=[  141],
     | 99.99th=[ 1205]
   bw (  KiB/s): min=21416, max=26544, per=100.00%, avg=23985.20, stdev=1151.93, samples=20
   iops        : min= 5354, max= 6636, avg=5996.30, stdev=287.98, samples=20
  write: IOPS=5981, BW=23.4MiB/s (24.5MB/s)(234MiB/10001msec); 0 zone resets
    slat (nsec): min=90, max=18415, avg=262.83, stdev=253.52
    clat (usec): min=55, max=27310, avg=93.98, stdev=222.53
     lat (usec): min=55, max=27310, avg=94.24, stdev=222.53
    clat percentiles (usec):
     |  1.00th=[   75],  5.00th=[   79], 10.00th=[   81], 20.00th=[   84],
     | 30.00th=[   87], 40.00th=[   89], 50.00th=[   91], 60.00th=[   93],
     | 70.00th=[   95], 80.00th=[   99], 90.00th=[  104], 95.00th=[  111],
     | 99.00th=[  124], 99.50th=[  133], 99.90th=[  167], 99.95th=[  208],
     | 99.99th=[ 2540]
   bw (  KiB/s): min=22480, max=26304, per=100.00%, avg=23926.40, stdev=1008.71, samples=20
   iops        : min= 5620, max= 6576, avg=5981.60, stdev=252.18, samples=20
  lat (usec)   : 50=0.16%, 100=91.10%, 250=8.72%, 500=0.02%, 750=0.01%
  lat (msec)   : 2=0.01%, 4=0.01%, 20=0.01%, 50=0.01%
  cpu          : usr=7.55%, sys=33.94%, ctx=119877, majf=0, minf=42
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=59963,59816,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=23.4MiB/s (24.6MB/s), 23.4MiB/s-23.4MiB/s (24.6MB/s-24.6MB/s), io=234MiB (246MB), run=10001-10001msec
  WRITE: bw=23.4MiB/s (24.5MB/s), 23.4MiB/s-23.4MiB/s (24.5MB/s-24.5MB/s), io=234MiB (245MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=0/116, sectors=0/35968, merge=0/1013, ticks=0/225, in_queue=231, util=0.13%
```
