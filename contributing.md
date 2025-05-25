# Contributing to Chat Dinger Configuration

When ChatGPT or Claude changes their interface, you can help by updating the configuration!

## How to Contribute

1. **Fork this repository**
2. **Update `config.json`** with new selectors
3. **Test your changes** with the Chat Dinger extension
4. **Submit a Pull Request** with details about what changed

## When to Update

- ChatGPT/Claude button selectors stop working
- New detection methods are needed
- Sites add new domains or change behavior

## Testing Your Changes

1. Update the config.json file
2. In Chat Dinger popup, click "🔄 Update" to fetch your changes
3. Test that notifications work on both sites
4. Submit PR if working correctly

## Configuration Format

### Adding New Sites
```json
"newsite": {
  "enabled": true,
  "domains": ["newsite.com"],
  "detection": {
    "method": "attribute_monitoring",
    "selectors": ["button[data-send]"],
    "stopKeywords": ["stop"],
    "sendKeywords": ["send"]
  }
}
