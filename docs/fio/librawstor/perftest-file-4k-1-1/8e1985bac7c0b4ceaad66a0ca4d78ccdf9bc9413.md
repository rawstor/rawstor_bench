[&lt; back](..)

# perftest-file-4k-1-1

2026-11-24 21:37:09

refs/heads/worktree-pki-show-positional

[8e1985b](https://github.com/rawstor/librawstor/commit/8e1985bac7c0b4ceaad66a0ca4d78ccdf9bc9413)

rw = randread, bs = 4k, iodepth = 1, numjobs = 1

```

randread: (groupid=0, jobs=1): err= 0: pid=16429: Tue Nov 24 21:36:02 2026
  read: IOPS=680k, BW=2658MiB/s (2787MB/s)(26.0GiB/10001msec)
    slat (nsec): min=164, max=55205, avg=222.64, stdev=264.40
    clat (nsec): min=561, max=95553, avg=1118.95, stdev=636.98
     lat (nsec): min=791, max=95772, avg=1341.59, stdev=705.92
    clat percentiles (nsec):
     |  1.00th=[  860],  5.00th=[  916], 10.00th=[  940], 20.00th=[  980],
     | 30.00th=[ 1020], 40.00th=[ 1048], 50.00th=[ 1080], 60.00th=[ 1112],
     | 70.00th=[ 1144], 80.00th=[ 1192], 90.00th=[ 1272], 95.00th=[ 1336],
     | 99.00th=[ 1496], 99.50th=[ 1608], 99.90th=[15936], 99.95th=[17792],
     | 99.99th=[22400]
   bw (  MiB/s): min= 2539, max= 2710, per=100.00%, avg=2659.76, stdev=44.13, samples=20
   iops        : min=650192, max=693786, avg=680898.40, stdev=11297.40, samples=20
  lat (nsec)   : 750=0.11%, 1000=25.96%
  lat (usec)   : 2=73.63%, 4=0.14%, 10=0.04%, 20=0.11%, 50=0.02%
  lat (usec)   : 100=0.01%
  cpu          : usr=37.36%, sys=62.62%, ctx=76, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=6805129,0,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1
randwrite: (groupid=1, jobs=1): err= 0: pid=16435: Tue Nov 24 21:36:02 2026
  write: IOPS=1780, BW=7121KiB/s (7292kB/s)(69.6MiB/10001msec); 0 zone resets
    slat (nsec): min=832, max=27528, avg=1521.48, stdev=975.27
    clat (usec): min=329, max=119248, avg=559.56, stdev=1378.43
     lat (usec): min=330, max=119249, avg=561.08, stdev=1378.55
    clat percentiles (usec):
     |  1.00th=[   400],  5.00th=[   429], 10.00th=[   449], 20.00th=[   474],
     | 30.00th=[   494], 40.00th=[   510], 50.00th=[   529], 60.00th=[   545],
     | 70.00th=[   562], 80.00th=[   586], 90.00th=[   619], 95.00th=[   652],
     | 99.00th=[   766], 99.50th=[   906], 99.90th=[  1303], 99.95th=[ 14615],
     | 99.99th=[100140]
   bw (  KiB/s): min= 4609, max= 7960, per=100.00%, avg=7124.35, stdev=875.06, samples=20
   iops        : min= 1152, max= 1990, avg=1780.95, stdev=218.80, samples=20
  lat (usec)   : 500=33.95%, 750=64.93%, 1000=0.84%
  lat (msec)   : 2=0.20%, 4=0.01%, 10=0.01%, 20=0.02%, 50=0.01%
  lat (msec)   : 100=0.02%, 250=0.01%
  cpu          : usr=0.76%, sys=1.53%, ctx=17806, majf=0, minf=36
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,17805,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
   READ: bw=2658MiB/s (2787MB/s), 2658MiB/s-2658MiB/s (2787MB/s-2787MB/s), io=26.0GiB (27.9GB), run=10001-10001msec

Run status group 1 (all jobs):
  WRITE: bw=7121KiB/s (7292kB/s), 7121KiB/s-7121KiB/s (7292kB/s-7292kB/s), io=69.6MiB (72.9MB), run=10001-10001msec

Disk stats (read/write):
  nvme0n1: ios=1/47837, sectors=8/1683024, merge=0/71009, ticks=1/97922, in_queue=97924, util=41.69%
```
