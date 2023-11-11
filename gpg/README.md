## Create a new keypair
`gpg --gen-key`

## Create a revocation certificate
`gpg --output ~/revocation.crt --gen-revoke your_email@address.com`

`chmod 600 ~/revocation.crt`

## Export the public key
`gpg --export --armor --output your-username-gpg.pub`

## Import public key
`gpg --import username-gpg.pub`

## Sign docs with detached signatures
`gpg --output doc.sig --detach-sig doc`

## Verify doc signature
`gpg --verify doc.sig doc`
