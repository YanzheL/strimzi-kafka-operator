FROM centos:7
ARG JAVA_VERSION=1.8.0

RUN yum -y update \
    && yum -y install \
        java-${JAVA_VERSION}-openjdk-headless \
        openssl \
    && yum -y clean all


# COPY --from=leeyanzhe/jvm:graalvm-ee-java11 /opt/ /opt/

# ENV LANG=en_US.UTF-8

# ENV JAVA_VERSION=11

# RUN set -eux \
#     && cd /opt/graalvm* \
#     && export JAVA_HOME="$(pwd)" \
#     # Set alternative links
#     && mkdir -p "/usr/java" \
#     && ln -sfT "$JAVA_HOME" /usr/java/default \
#     && ln -sfT "$JAVA_HOME" /usr/java/latest \
#     && for bin in "$JAVA_HOME/bin/"*; do \
#         base="$(basename "$bin")"; \
#         [ ! -e "/usr/bin/$base" ]; \
#         alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; \
#        done
