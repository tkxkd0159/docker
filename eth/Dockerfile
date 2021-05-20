FROM tkxkd0159/jsfocal:20.04
WORKDIR /app
RUN add-apt-repository -y ppa:ethereum/ethereum && \
    apt-get update && \
    apt-get install -y ethereum && mkdir data
COPY genesis-new.json ./
RUN geth init --datadir data genesis-new.json
CMD ["/bin/bash"]
EXPOSE 30303/tcp
EXPOSE 8545/tcp