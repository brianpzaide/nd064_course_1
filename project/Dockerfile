FROM python:2.7
WORKDIR /app
EXPOSE 3111
COPY techtrends/requirements.txt ./
RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get install -y sqlite3
RUN pip install -r requirements.txt
COPY techtrends/ .
RUN python init_db.py
CMD ["python", "app.py"]
