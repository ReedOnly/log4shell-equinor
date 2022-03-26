FROM python:3.9-slim

COPY . .

RUN pip install -r requirements.txt

CMD python3 poc.py --userip ubuntu --webport 8000 --lport 9001
