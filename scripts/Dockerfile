FROM python:3.8-slim

# Install dependencies
RUN pip install --upgrade pip && \
    pip install jupyter numpy pandas matplotlib seaborn lifelines

# Expose Jupyter default port
EXPOSE 8888

# Set the working directory
WORKDIR /app

# Command to run Jupyter Notebook
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
