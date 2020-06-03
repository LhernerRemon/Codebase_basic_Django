# Imagen base
FROM python:3.8-alpine
# establecer variables de entorno predeterminadas
ENV PYTHONUNBUFFERED 1 

RUN apk update \
  # psycopg2 dependencies
  && apk add --virtual build-deps gcc python3-dev musl-dev \
  && apk add postgresql-dev \
  # Pillow dependencies
  && apk add jpeg-dev zlib-dev freetype-dev lcms2-dev openjpeg-dev tiff-dev tk-dev tcl-dev \
  # CFFI dependencies
  && apk add libffi-dev py-cffi

# crear y establecer directorio de trabajo
RUN mkdir /app
WORKDIR /app

COPY ./requirements.txt /app/

# install environment dependencies
RUN pip install --upgrade pip \
    && pip install -r requirements.txt

COPY ./compose/django/entrypoint /entrypoint
RUN sed -i 's/\r//' /entrypoint
RUN chmod +x /entrypoint

COPY ./compose/django/start /start
RUN sed -i 's/\r//' /start
RUN chmod +x /start


# Agregar código de directorio actual al directorio de trabajo
COPY ["." , "/app/"]

ENTRYPOINT ["/entrypoint"]