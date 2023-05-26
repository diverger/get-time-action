# Get Time Action

Get the time in the specified time zone

## Example usage

```yaml
steps:
  - name: Get Time
    id: time
    uses: nanzm/get-time-action@master
    with:
      timeZone: UTC+8
      format: 'YYYY-MM-DD-HH-mm-ss'
  - name: Usage
    env:
      TIME: "${{ steps.time.outputs.time }}"
    run: |
      echo $TIME
```

## Inputs

| Parameter  | Required | Info                                                         |
| ---------- | -------- | ------------------------------------------------------------ |
| `timeZone` | `false`  | time Zone  Default: UTC                                        |
| `format`   | `false`  | timestamp format string  Default:                                   |

## Outputs

| Parameter   | Info                                                         |
| ---------- | ------------------------------------------------------------ |
| `time`   | time in the specified time zone|

## License

[MIT](LICENSE)
