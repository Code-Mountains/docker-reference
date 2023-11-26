# docker-reference
Commonly used docker commands for reference


# Docker Disk Storage info: 
```
$ docker system df
TYPE            TOTAL     ACTIVE    SIZE      RECLAIMABLE
Images          16        0         10.22GB   10.22GB (100%)
Containers      0         0         0B        0B
Local Volumes   26        0         9.002GB   9.002GB (100%)
Build Cache     94        13        273.7MB   270.9MB
```

# Docker Disk Storage info (Verbose): 
```
$ docker system df -v
Images space usage:

REPOSITORY                                       TAG                 IMAGE ID       CREATED        SIZE      SHARED SIZE   UNIQUE SIZE   CONTAINERS
course_practical_guide_eks-clients-api           latest              411f25c96255   2 hours ago    213MB     0B            213.2MB       0
custom-jfrog-router                              latest              67a21d90788b   22 hours ago   270MB     270.1MB       7.283kB       0
releases-docker.jfrog.io/jfrog/artifactory-pro   7.71.5              579d34721e0f   6 days ago     2.56GB    0B            2.565GB       0
jenkins/jenkins                                  lts                 6adc6425cd34   11 days ago    476MB     0B            476.2MB       0
releases-docker.jfrog.io/jfrog/xray-analysis     3.85.5              2c5c1601ad43   4 weeks ago    832MB     138.9MB       693MB         0
releases-docker.jfrog.io/jfrog/xray-persist      3.85.5              fbfbf85ac0d0   4 weeks ago    833MB     138.9MB       694.2MB       0
releases-docker.jfrog.io/jfrog/xray-indexer      3.85.5              27d9bb999b88   4 weeks ago    833MB     138.9MB       694.3MB       0
releases-docker.jfrog.io/jfrog/xray-server       3.85.5              86d0f59a37f4   4 weeks ago    1.63GB    138.9MB       1.487GB       0
rancher/rancher                                  latest              cb636b91766c   4 weeks ago    1.88GB    0B            1.881GB       0
nginx                                            stable-alpine       e6295d4bbc45   5 weeks ago    45.9MB    0B            45.91MB       0
releases-docker.jfrog.io/jfrog/router            7.81.0              5a1da95a64cd   7 weeks ago    270MB     270.1MB       0B            0
releases-docker.jfrog.io/jfrog/observability     1.17.0              c2e025de7984   2 months ago   338MB     0B            338MB         0
hello-world-nginx-app                            latest              3ceb749a9a1f   3 months ago   41.4MB    0B            41.39MB       0
releases-docker.jfrog.io/jfrog/xray-rabbitmq     3.11.9-management   94166b823848   9 months ago   269MB     0B            269.4MB       0
releases-docker.jfrog.io/postgres                13.10-alpine        433b3946ed35   9 months ago   238MB     0B            238MB         0
zobiz/xray-rabbitmq                              latest              0aaf0120f505   7 years ago    176MB     0B            175.9MB       0

Containers space usage:

CONTAINER ID   IMAGE     COMMAND   LOCAL VOLUMES   SIZE      CREATED   STATUS    NAMES

Local Volumes space usage:

VOLUME NAME                                                        LINKS     SIZE
48b92d009f7068b61e93da1931a4f3efba0e2cc26c0437b48c2077fc9688475c   0         4.909GB
505fde699f734565e57f2947cbbe9f1f79844a78034eecd71411eb67cdb70db4   0         0B
5e6dca130a6c6ddeb3df3dd23ca3d48219de1cfaafacef7453699f5e3efbec52   0         2.873kB
7ff329d26714f9f77217def7f09d64d5dc062c4c73545a925b37cfa9cd97a12a   0         2.873kB
0fcdbe38d19e440b797558fb3cd10b594f393fd710cc557710fde9e8de6670ef   0         556.3MB
29056d8a3fffec23f9f6bd3f28baa72ef236064eb7648332f242d04c0e7f7fbd   0         2.875kB
2b5453de815af37a4e3609f97cd4e2f866849269fbac4183f9a221743384420c   0         24.47kB
36cd2cd30413a977bdc02a932c86ae8c14d499a447e1ead6fe2580aa46a15670   0         54.32MB
5a32168d65310d13fd1e090ba119e7c7c5aab207054b8e5074db27cd43cc4220   0         405.2kB
860f91b257b70731e5c4572642e7cbb41bdafe11b22cf579f88934f190d74375   0         103MB
ab9915ad103e4d8df64931ab8f8ab5586d977b63a8f5503c9d399d1f2da5bca4   0         430.3kB
bdd18e2ee6ea17d3e0593edc13ea380eb722697fb388bcb618f7838bab770949   0         105.9MB
cc3bb157c8ac484542b1cc7b5333635799732e3c9ac6627badda00af81e24452   0         422.7kB
36dd79e577b19386d777f47a0d8b112321e4d140da23c37789ce3b808c15d7e2   0         2.283GB
9b118e091482125cf79524993923679e9b91d8b700493c1fd0e180410a6b5791   0         583.1kB
e8c8283f0530a8bf8f769c13755e67efe3aceb228ee52ca57f1da433c27fb5ef   0         0B
2a6f7936fb4cb809875a50c2d373dbb9cdb789471d9d80efd8858df1d86486a8   0         844B
4f46185c00240abfaf2d3895088619ff98deb04e0c736fce6981324cfd07890f   0         537.8MB
edbc0789998f4f14428747e28404528575b1ede23b2034e2f8ed51d4c6530ce3   0         431.9kB
f2f4c0496c03b6cb77e2d3f1b032c4dbf438f50297c41ac061f0ff3a6f39dde1   0         405.2kB
b93ef27c7a0b003038aeeb37eb6063889288847d191f07e497c0a3f4c21bf7cd   0         0B
61f1de9924710ecab9ee4460bb0b29b6bbecac516a00b8e94df3b6fa9e6a2532   0         54.32MB
259f6bbf9ecf5a299dc42663e08fd80a340cba061486067fe2953657193cf8a3   0         842B
9919d4ac4157937418ff248b3851211e645a4590c731231d0688680c2ed6d2ce   0         395.4MB
b06262ad3d29c720033b014b5ca81f52bb6baee4278fcba4bfdd12f33306c16f   0         844B
db7e72e6db52546b4b35e3b9bf8d2f3cfe9f020d97d85d9613698f89b8ea84fa   0         0B

Build cache usage: 273.7MB

CACHE ID        CACHE TYPE     SIZE      CREATED          LAST USED        USAGE     SHARED
aj0w4i5oa8el*   regular        244B      6 minutes ago                     0         false
coleip183jer*   regular        0B        6 minutes ago                     0         false
iybrwepl1wh8*   regular        2.63MB    6 minutes ago                     0         false
os4635nifmh5*   regular        305B      6 minutes ago                     0         false
oubnm5gkgm1d*   regular        0B        6 minutes ago                     0         false
p5buc71bbp04*   regular        78.7kB    6 minutes ago                     0         false
qw9948qb8tgy*   regular        184B      6 minutes ago                     0         false
v2tt2ouvb55n*   regular        0B        6 minutes ago                     0         false
y9uf393e0xbj*   regular        10.6kB    6 minutes ago                     0         false
xw2f7i7gbrtm    regular        0B        3 months ago     3 months ago     1         true
0eyc3t12l17y    regular        0B        3 months ago     3 months ago     1         true
nfhti1jt1y9s    regular        0B        3 months ago     3 months ago     1         true
i7lz7yt385c1    regular        0B        3 months ago     3 months ago     1         true
476f8zvoukz2    regular        0B        3 months ago     3 months ago     1         true
txmxgbk4swqo    regular        0B        3 months ago     3 months ago     1         true
lgmlnjunoiu3    regular        0B        3 months ago     3 months ago     1         true
1a7z0mu3zoxr    regular        305B      3 months ago     3 months ago     1         true
54m9qdoekxxt    regular        0B        3 months ago     3 months ago     1         true
mzgwo49t205g    regular        111B      3 months ago     3 months ago     1         true
vxp9nm53y9em    source.local   0B        3 months ago     3 months ago     1         false
ldcbb926o8pn    source.local   480B      3 months ago     3 months ago     1         false
lx0d6ae4lvyt    regular        0B        3 months ago     3 months ago     1         true
p3v9xazuv3nx    regular        0B        3 months ago     3 months ago     1         true
pez0mblmi2ry    source.local   416B      3 months ago     3 months ago     1         false
rzykt2a6ylyr    regular        0B        12 days ago      12 days ago      1         false
ab7xzhjbarje    regular        0B        12 days ago      12 days ago      1         false
v0pejscftkx1    regular        0B        12 days ago      12 days ago      1         false
acedvsvtcjg8    regular        0B        12 days ago      12 days ago      1         false
3pinr2u08zfx    regular        0B        12 days ago      12 days ago      1         false
vf7j5l57msc2    regular        0B        12 days ago      12 days ago      1         false
nsiq33iv9wi2    regular        105B      12 days ago      12 days ago      2         false
do5qvue25pgm    regular        0B        12 days ago      12 days ago      2         false
xcpt02r7uiqa    regular        465B      12 days ago      12 days ago      1         false
ozrco5kr3qhi    regular        20.5MB    12 days ago      12 days ago      2         false
wzurgdnq73lp    regular        0B        12 days ago      12 days ago      1         false
8zutp2tdh1fb    regular        0B        12 days ago      12 days ago      1         false
n78u3ri6myrm    regular        0B        12 days ago      12 days ago      1         false
tzriko3tnp4k    regular        0B        12 days ago      12 days ago      1         false
3j1fxt4v85yy    regular        0B        12 days ago      12 days ago      1         false
zfoeu33xt1t2    regular        0B        12 days ago      12 days ago      1         false
vanh9ydpdogg    regular        0B        12 days ago      12 days ago      1         false
pwinzc21afj5    regular        760B      12 days ago      12 days ago      1         false
svcc6sm66ilx    regular        0B        12 days ago      12 days ago      1         false
gew9xopt15aj    regular        20.2MB    12 days ago      12 days ago      1         false
la97wrpv98zb    regular        882B      12 days ago      12 days ago      1         false
gnfahqjjkyfs    regular        910B      12 days ago      12 days ago      2         false
xro7w5e9pswp    regular        911B      12 days ago      12 days ago      2         false
fiw4smovv6pw    regular        911B      12 days ago      12 days ago      2         false
sf5928uaa9aq    regular        945B      12 days ago      12 days ago      6         false
go8ihrxahnp4    regular        12.4MB    12 days ago      12 days ago      7         false
wzju7kn218y5    regular        946B      12 days ago      12 days ago      10        false
o18ifh02txz4    source.local   0B        12 days ago      12 days ago      29        false
9u8pvv0zbkah    source.local   527B      12 days ago      12 days ago      29        false
6zbpzltisnmr    source.local   946B      12 days ago      12 days ago      28        false
vom6pwml3ygo    regular        0B        22 hours ago     22 hours ago     1         true
ndw3vxuglmw0    regular        0B        22 hours ago     22 hours ago     1         true
ieqm72lxlw60    regular        0B        22 hours ago     22 hours ago     1         true
t3mhz3s6hehe    regular        0B        22 hours ago     22 hours ago     1         true
47xgzjzpnvr4    regular        0B        22 hours ago     22 hours ago     1         true
8ya2pypg8aqr    regular        0B        22 hours ago     22 hours ago     1         true
gao58fwt6ikz    regular        0B        22 hours ago     22 hours ago     1         true
xbi3em5a6lyo    regular        0B        22 hours ago     22 hours ago     3         true
uoe4i9ge287j    source.local   0B        22 hours ago     22 hours ago     4         false
7d9movyig9a8    source.local   391B      22 hours ago     22 hours ago     4         false
2f9b863moo8n    regular        4.56kB    22 hours ago     22 hours ago     2         true
elcv2e3l74km    regular        2.72kB    22 hours ago     22 hours ago     1         true
v7bb2p3sjcbp    regular        0B        3 hours ago      3 hours ago      1         false
vcujioayys6w    regular        19.5kB    3 hours ago      3 hours ago      1         false
0qss81c9seb7    regular        0B        2 hours ago      2 hours ago      1         true
opr2e0oemthu    regular        0B        2 hours ago      2 hours ago      1         true
6q6iih1p1w1x    regular        0B        2 hours ago      2 hours ago      1         true
pvlenbv9dnl3    regular        0B        2 hours ago      2 hours ago      1         true
igdb1gxjq65v    source.local   492B      3 hours ago      2 hours ago      2         false
0il06fe7juv3    regular        0B        2 hours ago      2 hours ago      1         true
vyz665kgr3xu    regular        18.2MB    2 hours ago      2 hours ago      1         false
wvme0hyuc7nu    regular        188MB     2 hours ago      2 hours ago      1         false
vkk1koxabt4l    regular        19.7kB    2 hours ago      2 hours ago      1         false
f0ws5zhd0dj7    source.local   7B        3 hours ago      2 hours ago      2         false
uceql797ztd2    regular        0B        2 hours ago      2 hours ago      1         true
tyovgcklcfl0    regular        0B        2 hours ago      2 hours ago      1         false
umvm9r77gybm    regular        11.6MB    2 hours ago      2 hours ago      1         false
x2yb0jqk288o    regular        5.52MB    2 hours ago      2 hours ago      1         true
lhn7cv1kxzfw*   regular        0B        2 hours ago      2 hours ago      1         false
r3ipqyiuk4f7*   regular        0B        2 hours ago      2 hours ago      1         false
1jpedll3rkh0*   regular        0B        2 hours ago      2 hours ago      1         false
rqbmc4zkpu3t    regular        0B        2 hours ago      2 hours ago      1         false
31yn53apnwaf    regular        0B        2 hours ago      2 hours ago      1         false
nlcullqzb4nf    regular        0B        2 hours ago      2 hours ago      1         false
c0vrm3lnj0wg    regular        0B        2 hours ago      2 hours ago      1         false
wpen89gklgs0    regular        0B        2 hours ago      2 hours ago      1         false
v1eby6gpu0q2    source.local   10.6kB    3 hours ago      2 hours ago      2         false
p36txdwp8gbc    regular        486kB     2 hours ago      21 minutes ago   2         false
wbrxs10jbz47*   regular        0B        2 hours ago      9 minutes ago    3         false
o7z40webfvj4    regular        55B       28 minutes ago   9 minutes ago    2         false
```