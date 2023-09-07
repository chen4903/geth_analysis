# 搭建阅读源码环境

推荐先学习完再`01.usage_console`再阅读源码，环境搭建也在其中。

可以使用vscode或者goland，运行rlp下的decode_test.go出现下面内容即成功搭建源码阅读环境

- vscode

```
Running tool: /usr/local/go/bin/go test -benchmem -run=^$ -coverprofile=/tmp/vscode-goLrzc3H/go-code-cover -bench . github.com/ethereum/go-ethereum/rlp

Running tool: /usr/local/go/bin/go test -timeout 30s -coverprofile=/tmp/vscode-goLrzc3H/go-code-cover github.com/ethereum/go-ethereum/rlp

ok  	github.com/ethereum/go-ethereum/rlp	0.022s	coverage: 96.3% of statements
goos: linux
goarch: amd64
pkg: github.com/ethereum/go-ethereum/rlp
cpu: AMD Ryzen 7 5800H with Radeon Graphics         
BenchmarkDecode-4                	     206	   5593443 ns/op	  52.58 MB/s	 2258360 B/op	      56 allocs/op
BenchmarkDecodeIntSliceReuse-4   	     297	   4458795 ns/op	  74.93 MB/s	   11404 B/op	       1 allocs/op
BenchmarkIntsize-4               	333124700	         4.014 ns/op	       0 B/op	       0 allocs/op
BenchmarkPutint-4                	29328169	        42.60 ns/op	      24 B/op	       1 allocs/op
BenchmarkEncodeBigInts-4         	  190807	      6400 ns/op	      24 B/op	       1 allocs/op
PASS
coverage: 35.5% of statements
ok  	github.com/ethereum/go-ethereum/rlp	8.910s
```

- goland

```
GOROOT=D:\Go\SDK #gosetup
GOPATH=D:\Go\goProject;C:\Users\ChenQin\go #gosetup
D:\Go\SDK\bin\go.exe test -c -o C:\Users\ChenQin\AppData\Local\Temp\GoLand\___decode_test_go__1_.test.exe github.com/ethereum/go-ethereum/rlp #gosetup
D:\Go\SDK\bin\go.exe tool test2json -t C:\Users\ChenQin\AppData\Local\Temp\GoLand\___decode_test_go__1_.test.exe -test.v -test.paniconexit0 -test.run ^\QTestStreamKind\E|\QTestNewListStream\E|\QTestStreamErrors\E|\QTestStreamList\E|\QTestStreamRaw\E|\QTestDecodeErrors\E|\QTestDecodeWithByteReader\E|\QTestDecodeWithEncReader\E|\QTestDecodeWithNonByteReader\E|\QTestDecodeStreamReset\E|\QTestDecodeDecoder\E|\QTestDecodeDecoderNilPointer\E|\QTestDecoderInByteSlice\E|\QTestDecoderFunc\E|\QExampleDecode\E|\QExampleDecode_structTagNil\E|\QExampleStream\E$ #gosetup
=== RUN   TestStreamKind
--- PASS: TestStreamKind (0.00s)
..........
=== RUN   ExampleDecode_structTagTail
--- PASS: ExampleDecode_structTagTail (0.00s)

=== RUN   ExampleDecode
--- PASS: ExampleDecode (0.00s)
=== RUN   ExampleDecode_structTagNil
--- PASS: ExampleDecode_structTagNil (0.00s)
=== RUN   ExampleStream
--- PASS: ExampleStream (0.00s)
PASS

Process finished with the exit code 0
```



















