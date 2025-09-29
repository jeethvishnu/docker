FROM mysql
ENV MYSQL_USER=expense \
    MYSQL_PASSWORD=ExpenseApp@1 \
    MYSQL_ROOT_PASSWORD=ExpenseApp@1 \
    MYSQL_DATABASE=transactions
COPY schema/*.sql /docker-entrypoint-initdb.d


