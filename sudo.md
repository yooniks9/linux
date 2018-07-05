## sudo without password
`echo '$USERNAME ALL=(ALL) NOPASSWD:ALL' | sudo tee -a /etc/sudoers.d/$USERNAME-init-user`