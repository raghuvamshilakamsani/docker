FROM python
WORKDIR /app
ADD . /app
RUN pip install --upgrade pip 
RUN python -m pip install pypi Flask
ENV NAME "World"
CMD ["python","app.py"]
