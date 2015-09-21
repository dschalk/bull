How is hover and focus possible if "it is not allowed to change the state during the computation of a reactive view." My rollover buttons alter button colors when the mouse pointer hovers over a button or selects it. How can I accomplish this effect without altering state?

The buttons are working, for now, but the console log says:

[mobservable.value '.Sbackground'] It is not allowed to change the state during the computation of a reactive view. (stack size is 2, active view: "ComputedObservable[.groupWatch:undefined] function groupWatch() {
	    if (this.group === 'GroupA' && this.test) {
	      mouseHandler.Abackground = 'green';
	      mouseHandler.Aborder = 'lawngreen';
	      mouseHandler.Acolor = 'yellow';
	      mouseHandler.Bbackground = '#000';
	      mouseHandler.Bborder = 'green';
	      mouseHandler.Bcolor = 'burlywood';
	      mouseHandler.Cbackground = '#000';
	      mouseHandler.Cborder = 'green';
	      mouseHandler.Ccolor = 'burlywood';
	      mouseHandler.Sbackground = '#000';
	      mouseHandler.Sborder = 'green';
	      mouseHandler.Scolor = 'burlywood';
	    } else if (this.group === 'GroupB' && this.test) {
	      mouseHandler.Bbackground = 'green';
	      mouseHandler.Bborder = 'lawngreen';
	      mouseHandler.Bcolor = 'yellow';
	      mouseHandler.Abackground = '#000';
	      mouseHandler.Aborder = 'green';
	      mouseHandler.Acolor = 'burlywood';
	      mouseHandler.Cbackground = '#000';
	      mouseHandler.Cborder = 'green';
	      mouseHandler.Ccolor = 'burlywood';
	      mouseHandler.Sbackground = '#000';
	      mouseHandler.Sborder = 'green';
	      mouseHandler.Scolor = 'burlywood';
	    } else if (this.group === 'GroupC' && this.test) {
	      mouseHandler.Cbackground = 'green';
	      mouseHandler.Cborder = 'lawngreen';
	      mouseHandler.Ccolor = 'yellow';
	      mouseHandler.Abackground = '#000';
	      mouseHandler.Aborder = 'green';
	      mouseHandler.Acolor = 'burlywood';
	      mouseHandler.Bbackground = '#000';
	      mouseHandler.Bborder = 'green';
	      mouseHandler.Bcolor = 'burlywood';
	      mouseHandler.Sbackground = '#000';
	      mouseHandler.Sborder = 'green';
	      mouseHandler.Scolor = 'burlywood';
	    } else if (this.group === 'solo' && this.test) {
	      mouseHandler.Sbackground = 'green';
	      mouseHandler.Sborder = 'lawngreen';
	      mouseHandler.Scolor = 'yellow';
	      mouseHandler.Abackground = '#000';
	      mouseHandler.Aborder = 'green';
	      mouseHandler.Acolor = 'burlywood';
	      mouseHandler.Bbackground = '#000';
	      mouseHandler.Bborder = 'green';
	      mouseHandler.Bcolor = 'burlywood';
	      mouseHandler.Cbackground = '#000';
	      mouseHandler.Cborder = 'green';
	      mouseHandler.Ccolor = 'burlywood';
	    } else if (this.test) {
	      mouseHandler.Abackground = '#000';
	      mouseHandler.Aborder = 'green';
	      mouseHandler.Acolor = 'burlywood';
	      mouseHandler.Bbackground = '#000';
	      mouseHandler.Bborder = 'green';
	      mouseHandler.Bcolor = 'burlywood';
	      mouseHandler.Cbackground = '#000';
	      mouseHandler.Cborder = 'green';
	      mouseHandler.Ccolor = 'burlywood';
	      mouseHandler.Sbackground = '#000';
	      mouseHandler.Sborder = 'green';
	      mouseHandler.Scolor = 'burlywood';
	    }
	  }")ObservableValue.set @ bundle.js:21847ObservableValue.asPropertyDescriptor.set @ bundle.js:21874groupWatch @ bundle.js:256ObservableView.compute @ bundle.js:21934ViewNode.computeNextState @ bundle.js:21076ViewNode.wakeUp @ bundle.js:21048ObservableView.get @ bundle.js:21905ObservableView.asPropertyDescriptor.get @ bundle.js:21974props.render @ bundle.js:325(anonymous function) @ bundle.js:22243(anonymous function) @ bundle.js:21256ObservableView.compute @ bundle.js:21934ViewNode.computeNextState @ bundle.js:21076ViewNode.wakeUp @ bundle.js:21048ViewNode.setRefCount @ bundle.js:21030sideEffect @ bundle.js:21193observeUntilInvalid @ bundle.js:21253d.componentWillMount.render @ bundle.js:22243ReactCompositeComponentMixin._renderValidatedComponentWithoutOwnerOrContext @ bundle.js:12256ReactCompositeComponentMixin._renderValidatedComponent @ bundle.js:12283ReactPerf.measure.wrapper @ bundle.js:3989ReactCompositeComponentMixin.mountComponent @ bundle.js:11704ReactPerf.measure.wrapper @ bundle.js:3989ReactReconciler.mountComponent @ bundle.js:4064mountComponentIntoNode @ bundle.js:9164Mixin.perform @ bundle.js:5114batchedMountComponentIntoNode @ bundle.js:9185Mixin.perform @ bundle.js:5114ReactDefaultBatchingStrategy.batchedUpdates @ bundle.js:16244batchedUpdates @ bundle.js:3641ReactMount._renderNewRootComponent @ bundle.js:9320ReactPerf.measure.wrapper @ bundle.js:3989ReactMount.render @ bundle.js:9409ReactPerf.measure.wrapper @ bundle.js:3989(anonymous function) @ bundle.js:541__webpack_require__ @ bundle.js:20Object.defineProperty.value @ bundle.js:49__webpack_require__ @ bundle.js:20(anonymous function) @ bundle.js:40(anonymous function) @ bundle.js:43
bundle.js:21848 console.trace()ObservableValue.set @ bundle.js:21848ObservableValue.asPropertyDescriptor.set @ bundle.js:21874groupWatch @ bundle.js:256ObservableView.compute @ bundle.js:21934ViewNode.computeNextState @ bundle.js:21076ViewNode.wakeUp @ bundle.js:21048ObservableView.get @ bundle.js:21905ObservableView.asPropertyDescriptor.get @ bundle.js:21974props.render @ bundle.js:325(anonymous function) @ bundle.js:22243(anonymous function) @ bundle.js:21256ObservableView.compute @ bundle.js:21934ViewNode.computeNextState @ bundle.js:21076ViewNode.wakeUp @ bundle.js:21048ViewNode.setRefCount @ bundle.js:21030sideEffect @ bundle.js:21193observeUntilInvalid @ bundle.js:21253d.componentWillMount.render @ bundle.js:22243ReactCompositeComponentMixin._renderValidatedComponentWithoutOwnerOrContext @ bundle.js:12256ReactCompositeComponentMixin._renderValidatedComponent @ bundle.js:12283ReactPerf.measure.wrapper @ bundle.js:3989ReactCompositeComponentMixin.mountComponent @ bundle.js:11704ReactPerf.measure.wrapper @ bundle.js:3989ReactReconciler.mountComponent @ bundle.js:4064mountComponentIntoNode @ bundle.js:9164Mixin.perform @ bundle.js:5114batchedMountComponentIntoNode @ bundle.js:9185Mixin.perform @ bundle.js:5114ReactDefaultBatchingStrategy.batchedUpdates @ bundle.js:16244batchedUpdates @ bundle.js:3641ReactMount._renderNewRootComponent @ bundle.js:9320ReactPerf.measure.wrapper @ bundle.js:3989ReactMount.render @ bundle.js:9409ReactPerf.measure.wrapper @ bundle.js:3989(anonymous function) @ bundle.js:541__webpack_require__ @ bundle.js:20Object.defineProperty.value @ bundle.js:49__webpack_require__ @ bundle.js:20(anonymous function) @ bundle.js:40(anonymous function) @ bundle.js:43
bundle.js:21847 [mobservable.value '.Sborder'] It is not allowed to change the state during the computation of a reactive view. (stack size is 2, active view: "ComputedObservable[.groupWatch:undefined] function groupWatch() {
	    if (this.group === 'GroupA' && this.test) {
	      mouseHandler.Abackground = 'green';
	      mouseHandler.Aborder = 'lawngreen';
	      mouseHandler.Acolor = 'yellow';
	      mouseHandler.Bbackground = '#000';
	      mouseHandler.Bborder = 'green';
	      mouseHandler.Bcolor = 'burlywood';
	      mouseHandler.Cbackground = '#000';
	      mouseHandler.Cborder = 'green';
	      mouseHandler.Ccolor = 'burlywood';
	      mouseHandler.Sbackground = '#000';
	      mouseHandler.Sborder = 'green';
	      mouseHandler.Scolor = 'burlywood';
	    } else if (this.group === 'GroupB' && this.test) {
	      mouseHandler.Bbackground = 'green';
	      mouseHandler.Bborder = 'lawngreen';
	      mouseHandler.Bcolor = 'yellow';
	      mouseHandler.Abackground = '#000';
	      mouseHandler.Aborder = 'green';
	      mouseHandler.Acolor = 'burlywood';
	      mouseHandler.Cbackground = '#000';
	      mouseHandler.Cborder = 'green';
	      mouseHandler.Ccolor = 'burlywood';
	      mouseHandler.Sbackground = '#000';
	      mouseHandler.Sborder = 'green';
	      mouseHandler.Scolor = 'burlywood';
	    } else if (this.group === 'GroupC' && this.test) {
	      mouseHandler.Cbackground = 'green';
	      mouseHandler.Cborder = 'lawngreen';
	      mouseHandler.Ccolor = 'yellow';
	      mouseHandler.Abackground = '#000';
	      mouseHandler.Aborder = 'green';
	      mouseHandler.Acolor = 'burlywood';
	      mouseHandler.Bbackground = '#000';
	      mouseHandler.Bborder = 'green';
	      mouseHandler.Bcolor = 'burlywood';
	      mouseHandler.Sbackground = '#000';
	      mouseHandler.Sborder = 'green';
	      mouseHandler.Scolor = 'burlywood';
	    } else if (this.group === 'solo' && this.test) {
	      mouseHandler.Sbackground = 'green';
	      mouseHandler.Sborder = 'lawngreen';
	      mouseHandler.Scolor = 'yellow';
	      mouseHandler.Abackground = '#000';
	      mouseHandler.Aborder = 'green';
	      mouseHandler.Acolor = 'burlywood';
	      mouseHandler.Bbackground = '#000';
	      mouseHandler.Bborder = 'green';
	      mouseHandler.Bcolor = 'burlywood';
	      mouseHandler.Cbackground = '#000';
	      mouseHandler.Cborder = 'green';
	      mouseHandler.Ccolor = 'burlywood';
	    } else if (this.test) {
	      mouseHandler.Abackground = '#000';
	      mouseHandler.Aborder = 'green';
	      mouseHandler.Acolor = 'burlywood';
	      mouseHandler.Bbackground = '#000';
	      mouseHandler.Bborder = 'green';
	      mouseHandler.Bcolor = 'burlywood';
	      mouseHandler.Cbackground = '#000';
	      mouseHandler.Cborder = 'green';
	      mouseHandler.Ccolor = 'burlywood';
	      mouseHandler.Sbackground = '#000';
	      mouseHandler.Sborder = 'green';
	      mouseHandler.Scolor = 'burlywood';
	    }
	  }")ObservableValue.set @ bundle.js:21847ObservableValue.asPropertyDescriptor.set @ bundle.js:21874groupWatch @ bundle.js:257ObservableView.compute @ bundle.js:21934ViewNode.computeNextState @ bundle.js:21076ViewNode.wakeUp @ bundle.js:21048ObservableView.get @ bundle.js:21905ObservableView.asPropertyDescriptor.get @ bundle.js:21974props.render @ bundle.js:325(anonymous function) @ bundle.js:22243(anonymous function) @ bundle.js:21256ObservableView.compute @ bundle.js:21934ViewNode.computeNextState @ bundle.js:21076ViewNode.wakeUp @ bundle.js:21048ViewNode.setRefCount @ bundle.js:21030sideEffect @ bundle.js:21193observeUntilInvalid @ bundle.js:21253d.componentWillMount.render @ bundle.js:22243ReactCompositeComponentMixin._renderValidatedComponentWithoutOwnerOrContext @ bundle.js:12256ReactCompositeComponentMixin._renderValidatedComponent @ bundle.js:12283ReactPerf.measure.wrapper @ bundle.js:3989ReactCompositeComponentMixin.mountComponent @ bundle.js:11704ReactPerf.measure.wrapper @ bundle.js:3989ReactReconciler.mountComponent @ bundle.js:4064mountComponentIntoNode @ bundle.js:9164Mixin.perform @ bundle.js:5114batchedMountComponentIntoNode @ bundle.js:9185Mixin.perform @ bundle.js:5114ReactDefaultBatchingStrategy.batchedUpdates @ bundle.js:16244batchedUpdates @ bundle.js:3641ReactMount._renderNewRootComponent @ bundle.js:9320ReactPerf.measure.wrapper @ bundle.js:3989ReactMount.render @ bundle.js:9409ReactPerf.measure.wrapper @ bundle.js:3989(anonymous function) @ bundle.js:541__webpack_require__ @ bundle.js:20Object.defineProperty.value @ bundle.js:49__webpack_require__ @ bundle.js:20(anonymous function) @ bundle.js:40(anonymous function) @ bundle.js:43
