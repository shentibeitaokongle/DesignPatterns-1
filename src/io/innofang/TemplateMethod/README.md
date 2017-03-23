# Template Method（模板方法）

在日常的开发中，模板方法是一种用于流程封装的设计模式

为了加深印象，可以类比一下平常在开发当中经常遇到的窘境：有一系列功能，功能的实现流程是固定的(比如，这个功能是先执行A，再执行B，最后执行C)，但是每个方法的具体实现细节是不一样的，如果没有一个良好的OOP设计思想，或许这时面对这种问题会直接在每个功能内部都实现相同的流程设计

但是如此设计显然是很不合理的，面对这种重复的流程，就考虑代码复用，才能使功能更加的健壮和简洁