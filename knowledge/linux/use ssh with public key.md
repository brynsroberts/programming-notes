To use SSH with a public key, you need to follow these steps:

1.  Generate an SSH key pair: You can generate a key pair using the ssh-keygen command on your local machine. The key pair consists of a private key and a public key. The private key should be kept secret, while the public key can be shared with others.

2.  Copy the public key to the remote server: You need to copy the public key to the remote server that you want to connect to. You can do this by appending the contents of the public key file (typically named id_rsa.pub) to the authorized_keys file on the remote server.

3.  Connect to the remote server using SSH: Once the public key is installed on the remote server, you can connect to it using SSH. To connect, you need to specify the path to the private key file (typically named id_rsa) using the -i option, and the username and hostname of the remote server.

Here's an example command for connecting to a remote server using SSH with a public key:

```bash
ssh -i /path/to/private/key user@hostname
```


Replace `/path/to/private/key` with the actual path to your private key file, `user` with the username of the remote server, and `hostname` with the actual hostname or IP address of the remote server.

If everything is set up correctly, you should be able to connect to the remote server without being prompted for a password.