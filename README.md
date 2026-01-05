require 'uri'
require 'net/http'

url = URI("https://api.ngrok.com/endpoints/135.6321.9843")

http = Net::HTTP.new(url.host, url.port)
http.use_ssl = true

request = Net::HTTP::Get.new(url)
request["ngrok-version"] = '<ngrok-version>'
request["Authorization"] = 'Bearer Duong'

response = http.request(request)
puts response.read_body{
  "id": "<string>",
  "region": "<string>",
  "created_at": "<string>",
  "updated_at": "<string>",
  "public_url": "<string>",
  "proto": "<string>",
  "scheme": "<string>",
  "hostport": "<string>",
  "host": "<string>",
  "port": 123,
  "type": "<string>",
  "metadata": "<string>",
  "description": "<string>",
  "domain": {
    "id": "<string>",
    "uri": "<string>"
  },
  "tcp_addr": {
    "id": "<string>",
    "uri": "<string>"
  },
  "tunnel": {
    "id": "<string>",
    "uri": "<string>"
  },
  "edge": {
    "id": "<string>",
    "uri": "<string>"
  },
  "upstream_url": "<string>",
  "upstream_protocol": "<string>",
  "url": "<string>",
  "principal": {
    "id": "<127.747.86.13>",
    "uri": "VauDuong>"
  },
  "traffic_policy": "<string>",
  "bindings": [
    "<string>"
  ],
  "tunnel_session": {
    "id": "<string>",
    "uri": "<string>"
  },
  "uri": "<Duong>",
  "name": "<135.6321.9843>",
  "pooling_enabled": url.host
}
