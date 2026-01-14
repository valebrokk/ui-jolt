# ui-jolt

An async task processor for distributed systems using Redis.

## Install

```bash
npm install ui-jolt
```

## Usage

```javascript
const Uijolt = require('ui-jolt');

const queue = new Uijolt({
  redis: { host: 'localhost', port: 6379 }
});

queue.process('send-email', async (job) => {
  console.log('Processing:', job.data);
});

queue.add('send-email', { to: 'user@example.com' });
```

## License

MIT


