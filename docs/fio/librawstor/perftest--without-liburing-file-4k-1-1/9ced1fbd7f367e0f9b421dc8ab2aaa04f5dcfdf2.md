[&lt; back](..)

# perftest--without-liburing-file-4k-1-1

2026-11-17 21:13:26

refs/heads/worktree-ref-tenant-to-account

[9ced1fb](https://github.com/rawstor/librawstor/commit/9ced1fbd7f367e0f9b421dc8ab2aaa04f5dcfdf2)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16338: Tue Nov 17 21:08:50 2026
  read: IOPS=402k, BW=1569MiB/s (1645MB/s)(15.3GiB/10001msec)
    slat (nsec): min=243, max=62974, avg=374.19, stdev=219.05
    clat (nsec): min=1131, max=67580, avg=1925.64, stdev=561.17
     lat (nsec): min=1393, max=67994, avg=2299.83, stdev=622.63
    clat percentiles (nsec):
     |  1.00th=[ 1336],  5.00th=[ 1400], 10.00th=[ 1464], 20.00th=[ 1576],
     | 30.00th=[ 1864], 40.00th=[ 1944], 50.00th=[ 1976], 60.00th=[ 2024],
     | 70.00th=[ 2064], 80.00th=[ 2096], 90.00th=[ 2160], 95.00th=[ 2224],
     | 99.00th=[ 2416], 99.50th=[ 2704], 99.90th=[10560], 99.95th=[12736],
     | 99.99th=[16768]
   bw (  MiB/s): min= 1523, max= 1597, per=100.00%, avg=1569.55, stdev=19.31, samples=20
   iops        : min=390010, max=408844, avg=401804.05, stdev=4944.43, samples=20
  lat (usec)   : 2=54.82%, 4=44.89%, 10=0.12%, 20=0.17%, 50=0.01%
  lat (usec)   : 100=0.01%
  cpu          : usr=56.80%, sys=43.18%, ctx=78, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=4016101,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16344: Tue Nov 17 21:08:50 2026
  write: IOPS=2279, BW=9119KiB/s (9338kB/s)(89.1MiB/10001msec); 0 zone resets
    slat (nsec): min=1074, max=36647, avg=3187.58, stdev=3650.37
    clat (usec): min=240, max=79040, avg=434.54, stdev=1025.77
     lat (usec): min=242, max=79050, avg=437.73, stdev=1025.90
    clat percentiles (usec):
     |  1.00th=[  302],  5.00th=[  326], 10.00th=[  343], 20.00th=[  363],
     | 30.00th=[  379], 40.00th=[  392], 50.00th=[  404], 60.00th=[  416],
     | 70.00th=[  433], 80.00th=[  453], 90.00th=[  482], 95.00th=[  510],
     | 99.00th=[  660], 99.50th=[  791], 99.90th=[ 1172], 99.95th=[18744],
     | 99.99th=[69731]
   bw (  KiB/s): min= 3136, max=10304, per=100.00%, avg=9123.15, stdev=1557.49, samples=20
   iops        : min=  784, max= 2576, avg=2280.70, stdev=389.36, samples=20
  lat (usec)   : 250=0.01%, 500=93.92%, 750=5.48%, 1000=0.46%
  lat (msec)   : 2=0.06%, 10=0.02%, 20=0.04%, 50=0.02%, 100=0.01%
  cpu          : usr=2.21%, sys=7.06%, ctx=45842, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,22799,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=1569MiB/s (1645MB/s), 1569MiB/s-1569MiB/s (1645MB/s-1645MB/s), io=15.3GiB (16.4GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=9119KiB/s (9338kB/s), 9119KiB/s-9119KiB/s (9338kB/s-9338kB/s), io=89.1MiB (93.4MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=3/60472, sectors=24/1923168, merge=0/89873, ticks=193/105764, in_queue=105960, util=46.31%
```
