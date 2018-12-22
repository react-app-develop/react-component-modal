## Install

```
npm i react-component-modal
```

## Usage

```
import CustomModal from 'react-component-modal';

constructor(props) {
    super(props);
    this.handleClose = this.handleClose.bind(this);
    this.closeModal = this.closeModal.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
    this.state = {
        visible: false
    };
}

render(){
  const { visible } = this.state;
  return (
    <CustomModal visible={visible} title="标题" negative_button_text="取消" positive_button_text="确定" hideModal={this.closeModal} handleSubmit={this.handleSubmit}>
        <div>
            <p>自定义内容</p>
        </div>
    </CustomModal>
  )
}

showModal() {
    this.setState({visible: true});
}
closeModal() {
    this.setState({visible: false});
}
handleSubmit() {
    this.setState({visible: false});
    //
}

```