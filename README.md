# Shipa GitHub Action

GitHub Action for managing cloud-native applications and policies on Kubernetes using Shipa

## Inputs

`shipa-action` - path to Shipa action yml file.

## Example usage

```yaml
  steps:
    - name: Checkout
      uses: actions/checkout@v2
    - name: Create shipa app
      uses: shipa-corp/shipa-gh-action@v0.0.1
      env:
        SHIPA_TOKEN: ${{ secrets.SHIPA_TOKEN }}
        SHIPA_HOST: ${{ secrets.SHIPA_HOST }}
      with:
        shipa-action: './example/shipa-action.yml'
```
