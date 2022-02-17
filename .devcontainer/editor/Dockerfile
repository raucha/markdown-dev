FROM plantuml/plantuml-server

# ARG USERNAME=vscode
# ARG USER_UID=1005
# ARG USER_GID=$USER_UID

USER root

RUN apt-get update && apt install -y npm wget pandoc wkhtmltopdf
RUN npm install -g puppeteer

WORKDIR /tmp
RUN wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
RUN apt install -y ./google-chrome-stable_current_amd64.deb
RUN chmod 777 /tmp/*

# USER jetty

# # # Create the user
# RUN groupadd --gid $USER_GID $USERNAME \
#     && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME \
#     #
#     # [Optional] Add sudo support. Omit if you don't need to install software after connecting.
#     && apt-get update \
#     && apt-get install -y sudo \
#     && echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
#     && chmod 0440 /etc/sudoers.d/$USERNAME

# # WORKDIR /documents

# # # [Optional] Set the default user. Omit if you want to keep the default as root.
# USER $USERNAME
