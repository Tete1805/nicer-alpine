FROM alpine:3.13
# add bash git sed nano grep and coreutils
RUN apk add --no-cache bash git sed nano grep coreutils
# install oh my bash
RUN bash -c "$(wget https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh -O -)"
# backup bashrc
RUN mv /root/.bashrc /root/.bashrc_old
# change theme
RUN sed 's/OSH_THEME=\"font\"/OSH_THEME=\"powerline-multiline\"/' /root/.bashrc_old >| /root/.bashrc