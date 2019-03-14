## Two useful patches for trafshow-5.2.3

### no-aggregate.patch

By default trafshow-5.2.3 auto-aggregates flows by /24 /16 /0 -masks if you have a lot of flows.  
With '-a 32' flag we can aggregate flows with /32 mask, but if you need to see all the flows (even with the same src and dest) separately, for example when you are testing speed by iperf with multiple streams, you can`t do it.  
With this patch you can disable aggregate at all by using the '-A' flag.

### sort_by_rate.patch

By default trafshow-5.2.3 sorts flows by Size/Data/Packets. With this patch trafshow will sort flows by CPS/PPS. 
