# sublimeSnippets

Here are the sublime snippets I think are worth sharing.

## Redux Component `rcc + <TAB>
```JS
import PropTypes from 'prop-types';
import React, {Component} from 'react';
import {connect} from 'react-redux';
import {
    action as actionAction,
} from 'path';

export class Component extends Component {
    static defaultProps = {
      prop: undefined,
    };
    
    static propTypes = {
      prop: PropTypes.arrayOf(PropTypes.string),
    };

    render() {
        const {
            action
        } = this.props;

        return (
            
        );
    }
}

export const mapStateToProps = ({state}) => ({
    prop: state.prop
});

export const mapDispatchToProps = (dispatch) => {
    return {
        action: () => {
            dispatch(actionAction());
        },
    };
};

export default connect(mapStateToProps, mapDispatchToProps)(Component);
```
