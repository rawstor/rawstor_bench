[&lt; back](..)

# perftest--without-liburing-ost-4k-1-1

2026-11-24 21:37:09

refs/heads/worktree-pki-show-positional

[8e1985b](https://github.com/rawstor/librawstor/commit/8e1985bac7c0b4ceaad66a0ca4d78ccdf9bc9413)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16716: Tue Nov 24 21:36:39 2026
  read: IOPS=10.0k, BW=39.1MiB/s (41.0MB/s)(391MiB/10001msec)
    slat (nsec): min=3357, max=44713, avg=4635.08, stdev=1615.09
    clat (usec): min=68, max=650, avg=93.88, stdev=15.03
     lat (usec): min=72, max=658, avg=98.52, stdev=15.89
    clat percentiles (usec):
     |  1.00th=[   76],  5.00th=[   78], 10.00th=[   79], 20.00th=[   80],
     | 30.00th=[   82], 40.00th=[   84], 50.00th=[   90], 60.00th=[  101],
     | 70.00th=[  104], 80.00th=[  106], 90.00th=[  112], 95.00th=[  121],
     | 99.00th=[  135], 99.50th=[  137], 99.90th=[  151], 99.95th=[  155],
     | 99.99th=[  169]
   bw (  KiB/s): min=35070, max=45056, per=100.00%, avg=40072.90, stdev=3234.14, samples=20
   iops        : min= 8767, max=11264, avg=10018.15, stdev=808.54, samples=20
  lat (usec)   : 100=58.39%, 250=41.60%, 500=0.01%, 750=0.01%
  cpu          : usr=20.79%, sys=24.17%, ctx=100150, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=100146,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16720: Tue Nov 24 21:36:39 2026
  write: IOPS=2121, BW=8488KiB/s (8691kB/s)(82.9MiB/10001msec); 0 zone resets
    slat (nsec): min=6983, max=40927, avg=9237.84, stdev=2596.29
    clat (usec): min=326, max=13527, avg=460.31, stdev=188.65
     lat (usec): min=334, max=13537, avg=469.54, stdev=188.77
    clat percentiles (usec):
     |  1.00th=[  355],  5.00th=[  371], 10.00th=[  383], 20.00th=[  404],
     | 30.00th=[  420], 40.00th=[  433], 50.00th=[  445], 60.00th=[  457],
     | 70.00th=[  469], 80.00th=[  490], 90.00th=[  519], 95.00th=[  562],
     | 99.00th=[  750], 99.50th=[ 1156], 99.90th=[ 2474], 99.95th=[ 4113],
     | 99.99th=[ 4948]
   bw (  KiB/s): min= 7936, max= 8841, per=100.00%, avg=8490.50, stdev=287.65, samples=20
   iops        : min= 1984, max= 2210, avg=2122.60, stdev=71.88, samples=20
  lat (usec)   : 500=84.85%, 750=14.15%, 1000=0.42%
  lat (msec)   : 2=0.42%, 4=0.10%, 10=0.05%, 20=0.01%
  cpu          : usr=5.92%, sys=5.97%, ctx=21236, majf=0, minf=37
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,21221,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=39.1MiB/s (41.0MB/s), 39.1MiB/s-39.1MiB/s (41.0MB/s-41.0MB/s), io=391MiB (410MB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=8488KiB/s (8691kB/s), 8488KiB/s-8488KiB/s (8691kB/s-8691kB/s), io=82.9MiB (86.9MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=1/54540, sectors=8/1297520, merge=0/82592, ticks=4/7875, in_queue=7880, util=27.07%
```
