[&lt; back](..)

# perftest-ost-4k-1-1

2026-11-17 21:13:26

refs/heads/worktree-ref-tenant-to-account

[9ced1fb](https://github.com/rawstor/librawstor/commit/9ced1fbd7f367e0f9b421dc8ab2aaa04f5dcfdf2)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16198: Tue Nov 17 21:08:29 2026
  read: IOPS=27.3k, BW=107MiB/s (112MB/s)(1068MiB/10001msec)
    slat (nsec): min=861, max=42164, avg=1011.74, stdev=368.75
    clat (usec): min=27, max=577, avg=35.34, stdev= 7.63
     lat (usec): min=28, max=578, avg=36.35, stdev= 7.67
    clat percentiles (usec):
     |  1.00th=[   31],  5.00th=[   32], 10.00th=[   32], 20.00th=[   33],
     | 30.00th=[   34], 40.00th=[   34], 50.00th=[   35], 60.00th=[   36],
     | 70.00th=[   36], 80.00th=[   37], 90.00th=[   39], 95.00th=[   43],
     | 99.00th=[   51], 99.50th=[   55], 99.90th=[  155], 99.95th=[  192],
     | 99.99th=[  293]
   bw (  KiB/s): min=100544, max=115792, per=100.00%, avg=109435.40, stdev=3763.89, samples=20
   iops        : min=25136, max=28948, avg=27358.75, stdev=940.99, samples=20
  lat (usec)   : 50=98.75%, 100=1.08%, 250=0.15%, 500=0.02%, 750=0.01%
  cpu          : usr=13.53%, sys=34.07%, ctx=273460, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=273457,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16199: Tue Nov 17 21:08:29 2026
  write: IOPS=2916, BW=11.4MiB/s (11.9MB/s)(114MiB/10001msec); 0 zone resets
    slat (nsec): min=1952, max=111017, avg=2544.31, stdev=1427.20
    clat (usec): min=240, max=28988, avg=340.00, stdev=193.59
     lat (usec): min=243, max=28991, avg=342.54, stdev=193.73
    clat percentiles (usec):
     |  1.00th=[  265],  5.00th=[  277], 10.00th=[  285], 20.00th=[  302],
     | 30.00th=[  314], 40.00th=[  322], 50.00th=[  330], 60.00th=[  338],
     | 70.00th=[  347], 80.00th=[  359], 90.00th=[  375], 95.00th=[  396],
     | 99.00th=[  594], 99.50th=[  873], 99.90th=[ 1614], 99.95th=[ 1876],
     | 99.99th=[ 4948]
   bw (  KiB/s): min=10512, max=12160, per=100.00%, avg=11671.70, stdev=483.86, samples=20
   iops        : min= 2628, max= 3040, avg=2917.75, stdev=120.93, samples=20
  lat (usec)   : 250=0.04%, 500=98.31%, 750=1.02%, 1000=0.23%
  lat (msec)   : 2=0.36%, 4=0.03%, 10=0.01%, 50=0.01%
  cpu          : usr=1.75%, sys=3.90%, ctx=29167, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,29167,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=107MiB/s (112MB/s), 107MiB/s-107MiB/s (112MB/s-112MB/s), io=1068MiB (1120MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=11.4MiB/s (11.9MB/s), 11.4MiB/s-11.4MiB/s (11.9MB/s-11.9MB/s), io=114MiB (119MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=2/75567, sectors=16/1702896, merge=0/113784, ticks=2/16628, in_queue=16631, util=35.32%
```
