[&lt; back](..)

# perftest-ost-4k-1-1

2025-10-24 07:31:18

refs/heads/ci/packages

[dbbc9bc](https://github.com/rawstor/librawstor/commit/dbbc9bcbb4cccdc4988920db56d816ba41b49be3)

rw = randrw, bs = 4k, iodepth = 1, numjobs = 1

```

rawstor: (groupid=0, jobs=1): err= 0: pid=11895: Fri Oct 24 07:31:15 2025
  read: IOPS=5957, BW=23.3MiB/s (24.4MB/s)(233MiB/10001msec)
    slat (nsec): min=40, max=15900, avg=173.68, stdev=210.19
    clat (usec): min=41, max=26203, avg=69.19, stdev=142.44
     lat (usec): min=41, max=26204, avg=69.37, stdev=142.44
    clat percentiles (usec):
     |  1.00th=[   51],  5.00th=[   55], 10.00th=[   57], 20.00th=[   60],
     | 30.00th=[   63], 40.00th=[   65], 50.00th=[   67], 60.00th=[   70],
     | 70.00th=[   73], 80.00th=[   76], 90.00th=[   83], 95.00th=[   90],
     | 99.00th=[  105], 99.50th=[  113], 99.90th=[  131], 99.95th=[  157],
     | 99.99th=[  408]
   bw (  KiB/s): min=22528, max=26400, per=100.00%, avg=23830.40, stdev=987.24, samples=20
   iops        : min= 5632, max= 6600, avg=5957.60, stdev=246.81, samples=20
  write: IOPS=5944, BW=23.2MiB/s (24.3MB/s)(232MiB/10001msec); 0 zone resets
    slat (nsec): min=80, max=21670, avg=245.74, stdev=275.29
    clat (usec): min=55, max=26939, avg=95.24, stdev=249.45
     lat (usec): min=56, max=26939, avg=95.49, stdev=249.45
    clat percentiles (usec):
     |  1.00th=[   73],  5.00th=[   78], 10.00th=[   81], 20.00th=[   84],
     | 30.00th=[   86], 40.00th=[   89], 50.00th=[   91], 60.00th=[   94],
     | 70.00th=[   96], 80.00th=[  101], 90.00th=[  109], 95.00th=[  115],
     | 99.00th=[  130], 99.50th=[  139], 99.90th=[  167], 99.95th=[  210],
     | 99.99th=[22152]
   bw (  KiB/s): min=22336, max=25808, per=100.00%, avg=23779.20, stdev=969.21, samples=20
   iops        : min= 5584, max= 6452, avg=5944.80, stdev=242.30, samples=20
  lat (usec)   : 50=0.34%, 100=88.50%, 250=11.13%, 500=0.02%, 750=0.01%
  lat (msec)   : 2=0.01%, 50=0.01%
  cpu          : usr=7.29%, sys=34.31%, ctx=119104, majf=0, minf=41
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=59576,59448,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=23.3MiB/s (24.4MB/s), 23.3MiB/s-23.3MiB/s (24.4MB/s-24.4MB/s), io=233MiB (244MB), run=10001-10001msec
  WRITE: bw=23.2MiB/s (24.3MB/s), 23.2MiB/s-23.2MiB/s (24.3MB/s-24.3MB/s), io=232MiB (243MB), run=10001-10001msec

Disk stats (read/write):
  sdb: ios=0/125, sectors=0/36592, merge=0/1076, ticks=0/281, in_queue=291, util=0.20%
```
