# Open API SDK for php developers

## Requirements

- PHP 5.3+

## Build

- to run unit tests, you will have to configure aliyun-sdk.properties files in your user directory, and make sure your project has corresponding service enabled, eg. openmr.

## Example

	include_once '../aliyun-php-sdk-core/Config.php';
	use Ecs\Request\V20140526 as Ecs;
	
	$iClientProfile = DefaultProfile::getProfile("cn-hangzhou", "<your accessKey>", "<your accessSecret>");
	$client = new DefaultAcsClient($iClientProfile);
	
	$request = new Ecs\DescribeRegionsRequest(); 
	$request->setMethod("GET");
	$response = $client->getAcsResponse($request);
	print_r($response);

## Authors && Contributors
- [liwqbj](https://github.com/liwqbj)

## License
