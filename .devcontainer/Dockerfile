FROM qmcgaw/latexdevcontainer:latest-full

USER root

RUN apt update -y --allow-releaseinfo-change && \
    apt install -y python3-pygments build-essential imagemagick

RUN chown -R vscode /workspace; \
    grep -v PDF /etc/ImageMagick-6/policy.xml > /tmp/policy.xml; sudo rm /etc/ImageMagick-6/policy.xml; sudo mv /tmp/policy.xml /etc/ImageMagick-6/policy.xml

USER vscode
