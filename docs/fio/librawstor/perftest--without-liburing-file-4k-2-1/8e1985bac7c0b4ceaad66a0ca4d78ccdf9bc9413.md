[&lt; back](..)

# perftest--without-liburing-file-4k-2-1

2026-11-24 21:37:09

refs/heads/worktree-pki-show-positional

[8e1985b](https://github.com/rawstor/librawstor/commit/8e1985bac7c0b4ceaad66a0ca4d78ccdf9bc9413)

rw = randread, bs = 4k, iodepth = 2, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16689: Tue Nov 24 21:36:35 2026
  read: IOPS=379k, BW=1479MiB/s (1551MB/s)(14.4GiB/10001msec)
    slat (nsec): min=270, max=145872, avg=391.02, stdev=321.79
    clat (usec): min=2, max=1246, avg= 4.66, stdev= 1.98
     lat (usec): min=3, max=1246, avg= 5.05, stdev= 2.01
    clat percentiles (nsec):
     |  1.00th=[ 2992],  5.00th=[ 3184], 10.00th=[ 3344], 20.00th=[ 3856],
     | 30.00th=[ 4192], 40.00th=[ 4320], 50.00th=[ 4448], 60.00th=[ 4512],
     | 70.00th=[ 4640], 80.00th=[ 4896], 90.00th=[ 6432], 95.00th=[ 7456],
     | 99.00th=[ 8032], 99.50th=[12096], 99.90th=[17536], 99.95th=[22144],
     | 99.99th=[80384]
   bw (  MiB/s): min= 1324, max= 1509, per=100.00%, avg=1480.10, stdev=42.96, samples=20
   iops        : min=339192, max=386378, avg=378905.85, stdev=10998.89, samples=20
  lat (usec)   : 4=23.74%, 10=75.63%, 20=0.55%, 50=0.07%, 100=0.01%
  lat (usec)   : 250=0.01%, 500=0.01%
  lat (msec)   : 2=0.01%
  cpu          : usr=53.69%, sys=46.28%, ctx=72, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=3787580,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2
randwrite: (groupid=1, jobs=1): err= 0: pid=16691: Tue Nov 24 21:36:35 2026
  write: IOPS=2950, BW=11.5MiB/s (12.1MB/s)(115MiB/10001msec); 0 zone resets
    slat (nsec): min=551, max=24936, avg=2031.45, stdev=1330.51
    clat (usec): min=210, max=17995, avg=674.84, stdev=343.73
     lat (usec): min=213, max=17996, avg=676.87, stdev=343.54
    clat percentiles (usec):
     |  1.00th=[  258],  5.00th=[  318], 10.00th=[  429], 20.00th=[  553],
     | 30.00th=[  586], 40.00th=[  611], 50.00th=[  635], 60.00th=[  660],
     | 70.00th=[  693], 80.00th=[  758], 90.00th=[  922], 95.00th=[ 1012],
     | 99.00th=[ 1614], 99.50th=[ 2606], 99.90th=[ 5342], 99.95th=[ 5866],
     | 99.99th=[ 7439]
   bw (  KiB/s): min=11168, max=12448, per=100.00%, avg=11806.20, stdev=395.73, samples=20
   iops        : min= 2792, max= 3112, avg=2951.40, stdev=98.92, samples=20
  lat (usec)   : 250=0.48%, 500=11.33%, 750=67.68%, 1000=14.87%
  lat (msec)   : 2=4.86%, 4=0.60%, 10=0.18%, 20=0.01%
  cpu          : usr=2.08%, sys=10.76%, ctx=59279, majf=0, minf=36
  IO depths    : 1=0.0%, 2=100.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,29507,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=2

Run status group 0 (all jobs):
   READ: bw=1479MiB/s (1551MB/s), 1479MiB/s-1479MiB/s (1551MB/s-1551MB/s), io=14.4GiB (15.5GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=11.5MiB/s (12.1MB/s), 11.5MiB/s-11.5MiB/s (12.1MB/s-12.1MB/s), io=115MiB (121MB), run=10001-10001msec

Disk stats (read/write):
  sda: ios=6/75549, sectors=48/2270344, merge=0/114541, ticks=77/14370, in_queue=14447, util=38.70%
```
