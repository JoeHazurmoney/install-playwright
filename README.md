# install-playwright
install playwright on rpm linux distros that are air-gapped from the internet

- symlink the role to /etc/ansible/roles or copy the role to /etc/ansible/roles
  - `sudo ln -s /home/taylorb/github/install-playwright/roles/playwright /etc/ansible/roles`

- run playbook
  - `ansible-playbook playbooks/install-playwright.yml -i inventory.yml -k -K -tag install-vscode`

## (optional) Download latest version of VSCode and VSCode Playwright extension
- Note: VSCode is not required to run Playwright
- Download rpm from: https://code.visualstudio.com/download
- copy .rpm to `roles/playwright/files`

- Download Playwright extension from: https://marketplace.visualstudio.com/items?itemName=ms-playwright.playwright
- copy .vsix to `roles/playwright/files`

## Run the role to install Playwright
`sudo ansible-playbook playbooks/install-playwright.yml -i inventory.yml -k -K --ask-vault-pass`