# Storm supervisior Docker file and system unit for storm based on centos 7

- the dockerfile is used to create a common storm supervisior. for each cluster, you need specific fleet unit files. for example, the storm cluster 1's unit file is storm1-sv@.service
- you can create mulitple instances for supervisior node at the same time for a cluster
- if you want to create supervisior for other storm cluster, you need to copy the fleet unit files and modify the storm cluster id (NBID) and the docker expose port. (in the start-sv script, it will adjust the port according to the cluster id)

   - cluster id=1, port list is from 6700-6709
   - cluster id=2, port list is from 6710-6719
   - and so on...
