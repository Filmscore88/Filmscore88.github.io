---
layout: post
title:      "Why we use DispatchToProps, and how we use it with Redux Thunk. "
date:       2019-08-20 15:24:13 +0000
permalink:  why_we_use_dispatchtoprops_and_how_we_use_it_with_redux_thunk
---



 We know that components are to be concerned only with displaying things.  Also, we should know that they are only to be getting their information from props.

Apart from the displaying of things which we have seen the components are responsible for, we are left with important functionality still, such as: 

1- How to get things to display
2- How you handle events. 

which is where containers come in to play. 


Take a look at this example of a well designed component:

```class FancyAlerter extends Component {
    sendAlert = () => {
        this.props.sendTheAlert()
    }

    render() {
        <div>
          <h1>Today's Fancy Alert is {this.props.fancyInfo}</h1>
          <Button onClick={sendAlert}/>
        </div>
     }
}```

See how this component gets the info it displays from props (which came from the redux store via mapStateToProps) and it also gets its action function from its props: sendTheAlert().

**Here is  where we have mapDispatchToProps  step in**:  Take a look at the following example:

```// FancyButtonContainer.js

function mapDispatchToProps(dispatch) {
    return({
        sendTheAlert: () => {dispatch(ALERT_ACTION)}
    })
}

function mapStateToProps(state) {
    return({fancyInfo: "Fancy this:" + state.currentFunnyString})
}

export const FancyButtonContainer = connect(
    mapStateToProps, mapDispatchToProps)(
    FancyAlerter
)```

Can you see how its the container that knows about redux, **dispatch**, store, state and  "stuff".

The FancyAlerter doesn't need to know about any of that "stuff" ,  it gets its method to call at onClick of the button, through its props.

**mapDispatchToProps  was the useful means that redux provides to let the container easily pass that function into the wrapped component on its props.
****

*So that brings us to the use of  **Thunk***

If Redux Thunk middleware is enabled, any time you attempt to dispatch a function instead of an action object, the middleware will call that function with dispatch method itself as the first argument.

 **Redux Thunk **teaches Redux to recognize special kinds of actions that are actually functions.
 
 
 Normally an action creator is returning an object but in case of thunk it returns and function where you can do some asynchronous work and when that work is completed,  then from that function you can return the object by calling dispatch method. 
 
 To sum it up, Thunk  is a  middleware by which one can perform anything before the action is going to the reducer but    it’s ideal for asynchronous type of work.








