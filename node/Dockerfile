# node 컨테이너 기반
FROM node


# 작업디렉토리를 생성하고 현 소스파일들을 전체를 붙여 넣는다.
WORKDIR /src
ADD . /src
USER root
# src 폴더로 이동한 다음에 패키지를 install 한다
RUN cd /src && npm install && npm install -g peer && chmod 700 /src/node.sh
# Expose port
EXPOSE 3030
EXPOSE 3031

# Run app
#CMD ["node", "/src/server.js"]
CMD ["/src/node.sh", "run"]