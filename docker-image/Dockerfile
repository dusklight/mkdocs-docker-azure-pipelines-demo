FROM python:3.8.1-alpine3.11
# I'm using a specific tag above because that's the version that's installed on my
# machine and I don't want to download any other images that would take up extra disk
# space (though it's not that much, about 100 MB).  Also, adjust as needed for Azure
# Piplines Agent's pre-installed images.

# Not needed unless we are using `mkdocs serve`.
EXPOSE 8000

# Git is required for the git-revision-date plugin.
RUN apk add git

RUN pip install --no-cache-dir mkdocs && \
    pip install --no-cache-dir mkdocs-material && \
    pip install --no-cache-dir mkdocs-git-revision-date-localized-plugin && \
    pip install --no-cache-dir pymdown-extensions

# Note that /mnt/repo should be the git root folder, not the content folder,
# otherwise the git-revision plugin will complain during build.
CMD ["/bin/sh", "-c", "cd /mnt/repo/content && mkdocs build"]

# To run this image as a container, first change to the root folder of the repository, then:
# * bash/linux:
# docker run --rm --mount type=bind,source=$(pwd),target=/mnt/repo <ThisImageNameAndTag>
# * Windows:
# docker run --rm --mount type=bind,source=%cd%,target=/mnt/repo <ThisImageNameAndTag>
