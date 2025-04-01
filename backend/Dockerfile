FROM python:3.13

# Set working directory
WORKDIR /

# Install dependencies
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

# Copy application code
COPY . .
RUN python create_db.py

# Expose the necessary port
EXPOSE 8000

# Use a proper entrypoint for production (remove --reload)
CMD ["uvicorn", "main:app", "--reload"]