FROM maven:3-jdk-8-slim

RUN apt update
RUN apt install -y python3 pip

COPY . .

RUN pip install -r requirements.txt

CMD python3 poc.py --userip ubuntu --webport 8000 --lport 9001
