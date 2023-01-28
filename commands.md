# View all Docker processes
docker ps -a

# Run Ubuntu docker image
docker run -it --name kubuntu ubuntu 

# Sample Output
dangolk@d3v ~ % docker run -it --name kubunut ubuntu
Unable to find image 'ubuntu:latest' locally
latest: Pulling from library/ubuntu
Digest: sha256:27cb6e6ccef575a4698b66f5de06c7ecd61589132d5a91d098f7f3f9285415a9
Status: Downloaded newer image for ubuntu:latest
root@d69d18bb1d53:/#

# Build Docker Image
docker build ./ -t explorecalifornia.com

# Run Docker Image
docker run --rm --name explorecalifornia.com -p 5000:80 explorecalifornia.com
docker run --rm --name explorecalifornia.com --publish
docker run --rm --name explorecalifornia.com -p
docker run --rm --name explorecalifornia.com -p  OUTSIDE:INSIDE
docker run --rm --name explorecalifornia.com -p  HOST:CONTAINER
docker run --rm --name explorecalifornia.com -p  5000:80
