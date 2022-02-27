# Logging

In the previous section we used some if-elif-else statements to add some input validation to our code. This checked that the SourceLanguageCode and TargetLanguageCode value were valid and printed a message.

Adding messages into our code that provide metadata information about how the code is executing is known as logging. Logs are useful in many ways. They can help pinpoint the flow of information in our code as well as where errors are being generated.

In this section we are going to use a function in python for logging. This is included in the core packages of python so we don't have to add it using pip, but can import it straight into our code.

The documentation for logging  provides prescriptive guidance on how to use the logging package

Logging allows us to define a number of different levels of logging. This helps to differentiate our different log messages when we conduct log file analysis.

From the documentation:

debug(msg, *args, **kwargs) - Logs a message with level DEBUG on the root logger.

info(msg, *args, **kwargs) - Logs a message with level INFO on this logger. The arguments are interpreted as for debug().

warning(msg, *args, **kwargs) - Logs a message with level WARNING on this logger. The arguments are interpreted as for debug().

error(msg, *args, **kwargs) - Logs a message with level ERROR on this logger. The arguments are interpreted as for debug().

critical(msg, *args, **kwargs) - Logs a message with level CRITICAL on this logger. The arguments are interpreted as for debug().

log(level, msg, *args, **kwargs) - Logs a message with integer level level on this logger. The other arguments are interpreted as for debug().

exception(msg, *args, **kwargs) - Logs a message with level ERROR on this logger. The arguments are interpreted as for debug(). Exception info is added to the logging message. This method should only be called from an exception handler.

Level	When it's used
DEBUG	Detailed information, typically of interest only when diagnosing problems.
INFO	Confirmation that things are working as expected.
WARNING	An indication that something unexpected happened, or indicative of some problem in the near future (e.g. ‘disk space low’). The software is still working as expected.
ERROR	Due to a more serious problem, the software has not been able to perform some function.
CRITICAL	A serious error, indicating that the program itself may be unable to continue running.
The default level is WARNING, which means that only events of this level and above will be tracked, unless the logging package is configured to do otherwise.

Events that are tracked can be handled in different ways. The simplest way of handling tracked events is to print them to the console. Another common way is to write them to a disk file.