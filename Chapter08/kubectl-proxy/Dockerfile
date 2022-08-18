FROM alpine/curl
RUN curl -L -O https://dl.k8s.io/v1.24.0/kubernetes-client-linux-arm64.tar.gz && \
tar zvxf kubernetes-client-linux-arm64.tar.gz kubernetes/client/bin/kubectl && \
mv kubernetes/client/bin/kubectl / && \
rm -rf kubernetes && \
rm -f kubernetes-client-linux-arm64.tar.gz
ADD kubectl-proxy.sh /kubectl-proxy.sh
ENTRYPOINT /kubectl-proxy.sh