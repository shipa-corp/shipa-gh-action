# Shipa GitHub Action

GitHub Action for managing cloud-native applications and policies on Kubernetes using Shipa

## Inputs

`shipa-action` - path to Shipa action yml file.

## Compatibility matrix

|                               | shipa < 1.6.3 | shipa >= 1.6.3 | 
|-------------------------------|-----------------|-----------------|
| `shipa-corp/shipa-gh-action@0.0.1`  | +               | -              |
| `shipa-corp/shipa-gh-action@0.0.2` | -               | +              |

## Example usage

```yaml
  steps:
    - name: Checkout
      uses: actions/checkout@v2
    - name: Create shipa app
      uses: shipa-corp/shipa-gh-action@0.0.2
      env:
        SHIPA_TOKEN: ${{ secrets.SHIPA_TOKEN }}
        SHIPA_HOST: ${{ secrets.SHIPA_HOST }}
      with:
        shipa-action: './example/shipa-action.yml'
``` 