Core Components:

TaskNet (Task Prediction Network):
A feedforward neural network responsible for classifying whether an individual's income exceeds $50K based on demographic and socioeconomic features. It uses a softmax output and is trained via cross-entropy loss to optimize prediction accuracy.

AuditNet (Fairness Auditing Network):
A secondary network designed to evaluate the output of TaskNet for potential bias. It takes the logits or output probabilities of TaskNet as input and produces a fairness compliance score. AuditNet is trained using binary cross-entropy to determine whether the prediction correlates with sensitive attributes.

Key Features:

Integrated Fairness Architecture: FAIR-TAN jointly trains TaskNet and AuditNet in a multi-objective setting, balancing prediction accuracy with ethical fairness.

Sensitive Attribute Supervision: The model explicitly incorporates sex (and can be extended to other protected attributes) to monitor and control disparate impact.

Ethical and Technical Evaluation: Predictions are assessed not only on accuracy but also on fairness criteria using demographic and statistical parity measures.
