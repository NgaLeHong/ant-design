---
order: 10
title:
  zh-CN: 可点击
  en-US: Clickable
---

## zh-CN

设置 `onChange` 后，Steps 变为可点击状态。

## en-US

Setting `onChange` makes Steps clickable.

```jsx
import { Steps, Divider } from 'antd';

const { Step } = Steps;

class Demo extends React.Component {
  state = {
    current: 0,
  };

  onChange = current => {
    console.log('onChange:', current);
    this.setState({ current });
  };

  render() {
    const { current } = this.state;

    return (
      <div>
        <Steps current={current} onChange={this.onChange}>
          <Step title="" description="This is a description." />
          <Step title="" description="This is a description." />
          <Step title="" description="This is a description." />
        </Steps>

        <Divider />

        <Steps current={current} onChange={this.onChange} direction="vertical">
          <Step title="" description="This is a description." />
          <Step title="" description="This is a description." />
          <Step title="" description="This is a description." />
        </Steps>
      </div>
    );
  }
}

ReactDOM.render(<Demo />, mountNode);
```
