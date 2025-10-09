# Use the official n8n image
FROM n8nio/n8n:latest

# Expose the port used by n8n
EXPOSE 5678

# Ensure that n8n is being called directly
ENTRYPOINT ["n8n"]

# Start n8n with the correct host binding
CMD ["start", "--host", "0.0.0.0", "--port", "5678"]
